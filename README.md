# Analysis of Publicly Available Skin Lesion Datasets 

This is a quick and brief analysis I made to examine publicly available skin lesion datasets and tasks, currently organized into six categories: Classical Classification, Segmentation Tasks, Dermoscopic Feature Detection, Temporal (longitudinal tracking), Vision-Language (image-text pairs), and Multi-modal (usually dermoscopic + clinical data) datasets. Each entry comes with the citation link, the dataset link and a brief description. More entries will be added soon. Each table is sorted by the dataset release year (oldest to newest).

## Table of Contents
- [1. Classical Classification Datasets](#1-classical-classification-datasets)
- [2. Segmentation Tasks](#2-segmentation-tasks)
- [3. Dermoscopic Feature Detection Tasks](#3-dermoscopic-feature-detection-tasks)
- [4. Temporal Datasets](#4-temporal-datasets)
- [5. Vision-Language Datasets](#5-vision-language-datasets)
- [6. Multi-modal Datasets](#6-multi-modal-datasets)

---

## 1. Classical Classification Datasets

Classification datasets consist of images with diagnostic labels, representing the most mature category with numerous validated datasets.


| Dataset | Images | Classes | Key Metadata | Modality | License | Notable Features |
|---------|--------|---------|--------------|----------|---------|------------------|
| **[PH² (2013)](https://doi.org/10.1109/EMBC.2013.6610779)** **[[data]](https://www.fc.up.pt/addi/ph2%20database.html)** | 200 | 3 (common nevus, atypical nevus, melanoma) | 8 dermoscopic criteria (colors, pigment network, dots/globules, streaks, regression areas, blue-whitish veil), asymmetry, clinical/histological diagnosis,  segmentation | Dermoscopic | Research only | comprehensive dermoscopic feature annotation by expert dermatologists |
| **[MED-NODE (2015)](https://doi.org/10.1016/j.eswa.2015.04.034)** **[[data]](http://www.cs.rug.nl/~imaging/databases/melanoma_naevi/)** | 170 | 2 (melanoma, nevus) | Limited | Clinical (non-dermoscopic) | Research |macroscopic images, 81% diagnostic accuracy |
| **[ISIC 2016 Task 3 (2016)](https://arxiv.org/abs/1605.01397)** **[[data]](https://challenge.isic-archive.com/landing/2016/)** | Train: 900, Test: 379 | 2 (benign, malignant) | Limited | Dermoscopic | CC-0 | 20% melanoma prevalence, histopathology ground truth|
| **[ISIC 2017 Task 3 (2017)](https://arxiv.org/abs/1710.05006)** **[[data]](https://challenge.isic-archive.com/landing/2017/)** | Train: 2,000, Val: 150, Test: 600 | 3 (Melanoma, Nevus, Seborrheic Keratosis) | Age, sex | Dermoscopic | CC-0 | Two independent binary classification subtasks, expanded dataset from ISIC 2016 |
| **[ISIC 2018 Task 3/ HAM10000 (2018)](https://doi.org/10.1038/sdata.2018.161)** **[[data]](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T)** | 10,015 | 7 (AKIEC, BCC, BKL, DF, MEL, NV, VASC) | Age, sex, anatomic location, lesion ID | Dermoscopic | CC-BY-NC | Multi-source (Vienna + Queensland), >50% histopathology confirmation |
| **[Derm7pt (2019)](https://doi.org/10.1109/JBHI.2018.2824327)** **[[data]](https://derm.cs.sfu.ca/Welcome.html)** | 1,011 cases (2,022+ images) | 2 + 7-point checklist | Age, sex, anatomic location, 7-point checklist scores (pigment network, blue whitish veil, vascular structures, pigmentation, streaks, dots/globules, regression structures) | Clinical + Dermoscopic | Research | paired imaging modalities (multimodal image for same lesion) |
| **[ISIC 2019 Challenge (2019)](https://challenge.isic-archive.com/landing/2019/)** **[[data]](https://www.kaggle.com/datasets/andrewmvd/isic-2019)** | 25,331 | 9 (8 known: MEL, NV, BCC, AK, BKL, DF, VASC, SCC + 1 unknown) | Age groups, anatomical site (8 sites), sex | Dermoscopic | CC-0 | Combined HAM10000, BCN20000, MSK datasets |
| **[PAD-UFES-20 (2020)](https://www.sciencedirect.com/science/article/pii/S235234092031115X)** **[[data]](https://data.mendeley.com/datasets/zr7vgbcyr2/1)** | 2,298 | 6 (BCC, SCC, MEL, ACK, SEK, NEV) | Age, region (15 sites), FST, diameter, clinical features | Clinical (smartphone) | Open access | Brazil dataset, 1,373 patients |
| **[ISIC 2020 / SIIM-ISIC (2020)](https://www.nature.com/articles/s41597-021-00815-z)** **[[data]](https://challenge2020.isic-archive.com/)** | 33,126 | 2 (melanoma, benign) | anatomical site, age, sex, patient-level context | Dermoscopic | CC-BY-NC 4.0 | patient-centric dataset; 2,056 patients |
| **[Fitzpatrick 17k (2021)](https://arxiv.org/abs/2104.09957)** **[[data]](https://github.com/mattgroh/fitzpatrick17k)** | 16,577 (4,744 skin lesions) | 114 skin conditions | FST (I-VI), diagnosis| Clinical | Open source |  Atlas Dermatologico + DermaAmin|
| **[DDI - Diverse Dermatology Images (2022)](https://www.science.org/doi/10.1126/sciadv.abq6147)** **[[data]](https://ddi-dataset.github.io/)** | 656 | 2 (benign, malignant) | FST (I-VI), age, gender, pathology confirmation | Clinical | Research use agreement | diverse skin tones, 570 patients, designed for skin tone bias evaluation |
| **[Hospital Italiano de Buenos Aires (2023)](https://www.nature.com/articles/s41597-023-02630-0)** **[[data]](https://doi.org/10.34970/587329)** |  1,616 (1,270 derm + 346 clinical) | 10 (MM, BCC, SCC, AK, NV, SK, SL, LK, DF, VASC) | Age, sex, Fitzpatrick skin type, anatomic site, personal/family history of melanoma, diagnosis confirmation method | Dermoscopic + Clinical | CC-BY | Argentina/Hispanic America population |
| **[PROVe-AI Dataset (2023)](https://www.nature.com/articles/s41746-023-00872-1)** **[[data]](https://api.isic-archive.com/doi/prove-ai/)** | 603 | 2 (melanoma: 95, non-melanoma: 508) | Age, sex, anatomic site, Fitzpatrick skin type, nevus phenotype, personal/family history | Dermoscopic | CC-0 (via ISIC) | 100% biopsy-confirmed, prospective clinical validation, real-world suspicious lesions from MSKCC |
| **[PASSION Dataset (2024)](https://link.springer.com/chapter/10.1007/978-3-031-72384-1_66)** **[[data]](https://passionderm.github.io/#Dataset)** | 4,901 | various skin conditions | FST (III-VI) | Clinical | CC-BY-NC | Sub-Saharan African population |
| **[SCIN (2024)](https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2826506)** **[[data]](https://github.com/google-research-datasets/scin)** | 10,408 | 419 SNOMED-CT categories | FST, Monk Skin Tone, demographics | Smartphone clinical | Custom SCIN License | Crowdsourced, early-stage conditions (54% <7 days onset) |
| **[ISIC 2024 / SLICE-3D (2024)](https://www.nature.com/articles/s41597-024-03743-w)** **[[data]](https://challenge2024.isic-archive.com/)** | Train: 401,059, Test: ~500,000 | Binary (malignant/benign) | 3D location, demographics | 3D-TBP crops | CC-BY-NC/CC-BY | Non-dermoscopic, addresses selection bias, 92-camera system |
| **[DERM12345 (2024)](https://pubmed.ncbi.nlm.nih.gov/39609462/)** **[[data]](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DAXZ7P)** | 12,345 | 40 subclasses (3-level hierarchy) | Age, sex, location, device info | Dermoscopic | CC-BY 4.0 | Most detailed hierarchical taxonomy, Turkey population |
| **[BCN20000 (2024)](https://www.nature.com/articles/s41597-024-03387-w)** **[[data]](https://api.isic-archive.com/collections/249/)** | Train: 12,413, Test: 6,533 | 8 + OOD class (NV, MEL, BCC, SK, AK, SCC, DF, VASC) | Age, sex, anatomic site, date | Dermoscopic | CC BY 4.0 | "Lesions in the wild", challenging tertiary cases (nails, mucosa) |
| **[Mpox Skin Lesion v2.0 (2024)](https://arxiv.org/abs/2306.14169)**  **[[data]](https://www.kaggle.com/datasets/joydippaul/mpox-skin-lesion-dataset-version-20-msld-v20)**| 755 | 6 (Mpox, Chickenpox, etc.) | Patient ID, validation status | Clinical | CC-BY 4.0 | Emerging infectious disease focus |
| **[DermaCon-IN (2025)](https://arxiv.org/abs/2506.06099)** **[[data]](https://datasetcatalog.nlm.nih.gov/dataset?q=0002117568)** | 5,450+ | 240+ diagnoses (hierarchical taxonomy) | Anatomic location, skin lesion descriptors, FST, Monk skin tone, age, sex, diagnostic certainty, hierarchical Rook's classification (8 main classes, multiple subclasses) | Clinical | CC-BY-NC-SA 4.0 | South India outpatient population (~3,000 patients), regional disease patterns (fungal, viral, parasitic infections) |


---

## 2. Segmentation Tasks

Segmentation tasks focus on precise lesion boundary detection, essential for automated analysis and feature extraction.

| Dataset/Task | Images | Annotation Type |  Modality | License | Notable Features |
|--------------|----------------|-----------------|-------|---------|------------------|
| **[PH² (2013)](https://doi.org/10.1109/EMBC.2013.6610779)** **[[data]](https://www.fc.up.pt/addi/ph2%20database.html)** | 200 (29 with color masks) | Binary masks; Color class masks (6 colors: white, red, light-brown, dark-brown, blue-gray, black)  | Dermoscopic | Research only | Color class segmentation available for subset of 29 images |
| **[ISIC 2016 Task 1 (2016)](https://arxiv.org/abs/1605.01397)** **[[data]](https://challenge.isic-archive.com/landing/2016/37/)** | Train: 900, Test: 379 | Binary masks (PNG) | Dermoscopic | CC-0 | |
| **[ISIC 2017 Task 1 (2017)](https://arxiv.org/abs/1710.05006)** **[[data]](https://challenge.isic-archive.com/landing/2017/42/)** | Train: 2,000, Val: 150, Test: 600 | Binary masks (PNG) | Dermoscopic | CC-0 |
| **[iToBoS Detection (2025)](https://doi.org/10.1038/s41597-025-05483-x)** **[[data_1]](https://www.kaggle.com/competitions/itobos-2024-detection/)** **[[data_2]](https://doi.org/10.6084/m9.figshare.28452545)** | Train: 8,473;   Test: 8,481 | Bounding box annotations; YOLO and COCO format | 3D-TBP tiles | CC-BY 4.0 | Skin region tiles with multiple lesions per image in natural anatomical context |
| **[SLICE-3D / ISIC 2024 (2024)](https://doi.org/10.1038/s41597-024-03743-w)** **[[data]](https://challenge2024.isic-archive.com/)** | Train: 401,059 | 15mm×15mm image crops with metadata | 3D-TBP crops | CC-BY-NC / CC-BY | smartphone-like images; multi-center data from 7 institutions|

---

## 3. Dermoscopic Feature Detection Tasks

These tasks identify specific dermoscopic structures critical for clinical diagnosis using established dermoscopic criteria.

| Dataset | Images | Features Annotated | Modality | License | Notable Features |
|---------|--------|-------------------|----------|---------|------------------|
| **[PH² (2013)](https://doi.org/10.1109/EMBC.2013.6610779)** **[[data]](https://www.fc.up.pt/addi/ph2%20database.html)** | 200 | Pigment network (T/AT), Dots/globules (A/T/AT), Streaks (P/A), Regression areas (P/A), Blue-whitish veil (P/A), Colors (6 classes: white, red, light-brown, dark-brown, blue-gray, black), Asymmetry | Dermoscopic | Research only | *Notes: P: present, A: absent, T: typical, AT: atypical;  Subset of 29 images with color class segmentation masks |
| **[ISIC 2016 Task 2 (2016)](https://arxiv.org/abs/1605.01397)** **[[data]](https://challenge.isic-archive.com/landing/2016/38/)** | Train: 807, Test: 335 | Superpixel-level annotations: Globules (presence/absence per superpixel), Streaks (presence/absence per superpixel) | Dermoscopic | CC-0 | superpixel-level annotations with cross-validation; SLIC superpixel subdivision |
| **[ISIC 2017 Part 2 (2017)](https://arxiv.org/abs/1710.05006)** **[[data]](https://challenge.isic-archive.com/landing/2017/43/)** | Train: 2,000, Val: 150, Test: 600 | Superpixel-level annotations: Pigment Network, Negative Network, Streaks, Milia-like Cysts | Dermoscopic | CC-0 | Superpixel-level feature for four key dermoscopic criteria|
| **[ISIC 2018 Task 2 (2018)](https://doi.org/10.1038/sdata.2018.161)** **[[data]](https://challenge.isic-archive.com/landing/2018/46/)** | 2,594 | Superpixel-level annotations: Pigment Network, Negative Network, Streaks, Milia-like Cysts, Globules | Dermoscopic | CC-0 | added Globules annotation and more training data to ISIC 2017 |
| **[Derm7pt (2019)](https://doi.org/10.1109/JBHI.2018.2824327)** **[[data]](https://derm.cs.sfu.ca/Welcome.html)** | 1,011 cases (2,022 images) | 7-point checklist: Pigment network, Blue-whitish veil, Vascular structures, Pigmentation, Streaks, Dots/globules, Regression structures + metadata (diagnostic difficulty, elevation, location, sex) | Clinical + Dermoscopic | Research | Paired imaging modalities (clinical and dermoscopic)|
---

## 4. Temporal Datasets

Temporal datasets contain multiple images of the same lesion over time, enabling change detection research. This category remains critically underdeveloped.

| Dataset | Participants/Images | Temporal Characteristics | Modality | Key Metadata | License | Notable Features |
|---------|---------------------|-------------------------|----------|--------------|---------|------------------|
| **[UQ Longitudinal Dataset (2025)](https://doi.org/10.1038/s41597-025-05880-2)** **[[data]](https://doi.org/10.48610/a13deaf)** | 480 participants; 250,162 tile images; 35,909 dermoscopic images | 340 participants with 2-7 timepoints; 6-month intervals; 2-3 year follow-up | 3D-TBP tiles + Dermoscopic | Age, sex, anatomic location, naevi count, skin/eye/hair color, freckling, ancestry, sun exposure, skin cancer history | CC-BY-NC-ND 4.0 | Paired tile and dermoscopic images of same lesions (9,389 unique lesions with 30 melanomas) |
| **[SDDI1 (Basel) (2025)](https://doi.org/10.1038/s41591-025-03747-y)** **[[data]](https://api.isic-archive.com/collections/328/)** | 66 patients; 585 dermoscopic images (116 lesions) | Short-term monitoring; ~3-month intervals for change detection | Dermoscopic | Binary change labels (changed vs. stable); lesion diagnosis | CC-BY-NC | sequence length=5 |
| **[SDDI2 (Vienna) (2025)](https://doi.org/10.1038/s41591-025-03747-y)**[private] | 229 sequential lesions; 458 dermoscopic images | Short-term sequential monitoring | Dermoscopic | Binary change labels and fine-grained malignant change labels | N/A | Includes malignant change annotations, sequence length=2; from PanDerm team |
| **[SDDI_Alfred (2025)](https://doi.org/10.1038/s41591-025-03747-y)**[private] | 122 patients; 730 dermoscopic images (179 serial sequences) | Long-term monitoring from 2007-2019  | Dermoscopic | Age, gender, anatomic location, diagnosis (89 melanomas: 34 invasive, 55 in situ; 90 benign) | N/A | sequence length = 1-12, avg ~4 ; from PanDerm team |


---

## 5. Vision-Language Datasets

Image-text and VQA datasets emerged rapidly to support vision-language model development in dermatology.

| Dataset | Year | Image-Text Pairs | Unique Images | Text Type | Key Features | License | Access Link | Notable Achievements |
|---------|------|------------------|---------------|-----------|--------------|---------|-------------|---------------------|
to be added soon


---

## 6. Multi-modal Datasets

Multi-modal datasets capture the same lesion with different imaging modalities, supporting fusion learning and cross-modal analysis.

| Dataset | Year | Total Images | Lesions | Modalities | Key Metadata | Ground Truth | License | Access Link | Notable Features |
|---------|------|--------------|---------|------------|--------------|--------------|---------|-------------|------------------|
to be added soon


---

## Dataset Licensing 

| License Type | Commercial Use | Attribution | Share-Alike | Modifications |
|--------------|----------------|-------------|-------------|---------------|
| **CC-0** | Yes | Optional | No | Allowed |
| **CC-BY 4.0** | Yes | Required | No | Allowed |
| **CC-BY-NC** | No | Required | No | Allowed |
| **CC-BY-NC-ND** | No | Required | No | Not allowed |
| **Research Only** | No | Varies | N/A | Usually allowed |
---

## Contributing

Contributions to this collection of skin lesion datasets and tasks or any suggestions to fix/adjust existing entries are welcome! 

## Contact
Ping-Cheng Ku (pku1@jh.edu)
# Collection and Analysis of Skin Lesion Datasets

This catalog surveys skin-lesion and broader dermatology image datasets across classification, segmentation and detection, dermoscopic features, temporal tracking, vision-language tasks, paired multimodal imaging, skin-tone/fairness research, and dermatopathology. It prioritizes official dataset records and primary papers; a resource may appear in more than one task table when its annotations support multiple uses.

**Last source review:** 2026-07-16.

The year in a dataset name is the first public dataset release year when that date is known. If only a paper or challenge year is established, the notes say so. `License / access` describes the dataset rather than the article; public article access does not imply open data reuse. Always recheck the linked terms before downloading or redistributing data.

Coverage is release-oriented: the catalog includes named datasets with a stable primary paper or authoritative description and a canonical access record. It does not enumerate every raw ISIC source collection, private evaluation cohort, synthetic-only derivative, benchmark repackage, or legacy dataset whose current provenance or reuse terms cannot be verified.

## Table of Contents

- [1. Classical Classification Datasets](#1-classical-classification-datasets)
- [2. Segmentation and Detection Tasks](#2-segmentation-and-detection-tasks)
- [3. Dermoscopic Feature and Concept Annotations](#3-dermoscopic-feature-and-concept-annotations)
- [4. Temporal Datasets](#4-temporal-datasets)
- [5. Vision-Language Datasets](#5-vision-language-datasets)
- [6. Paired Multimodal Datasets](#6-paired-multimodal-datasets)
- [7. Skin-Tone and Fairness Resources](#7-skin-tone-and-fairness-resources)
- [8. Dermatopathology Datasets](#8-dermatopathology-datasets)
- [Access and licensing notes](#access-and-licensing-notes)

---

## 1. Classical Classification Datasets

Classification datasets provide diagnostic or condition labels. Counts distinguish images, lesions, and patients where the primary source makes that distinction available.

| Dataset | Images / cases | Classes | Key metadata | Modality | License / access | Notable features |
| --- | --- | --- | --- | --- | --- | --- |
| **[PH² (2013)](https://doi.org/10.1109/EMBC.2013.6610779)** **[[data]](https://www.fc.up.pt/addi/ph2%20database.html)** | 200 images | 3 | Dermoscopic criteria, asymmetry, diagnosis, masks | Dermoscopic | Research use | Expert feature annotations and lesion masks |
| **[MED-NODE (2015)](https://doi.org/10.1016/j.eswa.2015.04.034)** **[[data]](https://www.cs.rug.nl/~imaging/databases/melanoma_naevi/)** | 170 images | 2 (melanoma, nevus) | Limited visual attributes | Clinical | Research use; check site terms | Standard-camera macroscopic images |
| **[ISIC 2016 Task 3 (2016)](https://arxiv.org/abs/1605.01397)** **[[data]](https://challenge.isic-archive.com/landing/2016/)** | Train 900; test 379 | 2 | Limited | Dermoscopic | Check collection-level ISIC terms | Histopathology-backed melanoma challenge |
| **[ISIC 2017 Task 3 (2017)](https://arxiv.org/abs/1710.05006)** **[[data]](https://challenge.isic-archive.com/landing/2017/)** | Train 2,000; validation 150; test 600 | 3 | Age, sex | Dermoscopic | Check collection-level ISIC terms | Expanded melanoma, nevus, and seborrheic-keratosis task |
| **[HAM10000 / ISIC 2018 Task 3 (2018)](https://doi.org/10.1038/sdata.2018.161)** **[[data]](https://doi.org/10.7910/DVN/DBW86T)** | 10,015 images | 7 | Age, sex, site, lesion ID | Dermoscopic | CC BY-NC 4.0 | Multi-source dataset; more than half histopathology-confirmed |
| **[Derm7pt (2019 issue; online 2018)](https://doi.org/10.1109/JBHI.2018.2824327)** **[[data]](https://derm.cs.sfu.ca/Welcome.html)** | 1,011 cases; paired images | Diagnosis + 7-point checklist | Age, sex, site, checklist scores | Clinical + dermoscopic | Research use; check site terms | Paired modalities for the same lesion |
| **[ISIC 2019 Challenge (2019)](https://arxiv.org/abs/1902.03368)** **[[data]](https://challenge.isic-archive.com/landing/2019/)** | 25,331 training images | 8 known classes + unknown/OOD | Age group, site, sex | Dermoscopic | Mixed source/collection terms | Combines HAM10000, BCN20000, and MSK data; overlaps other rows |
| **[PAD-UFES-20 (2020)](https://arxiv.org/abs/2007.00478)** **[[data]](https://data.mendeley.com/datasets/zr7vgbcyr2/1)** | 2,298 images; 1,641 lesions; 1,373 patients | 6 | Up to 21 clinical fields, including age, site, FST, diameter | Smartphone clinical | CC BY 4.0 | Brazilian cohort with patient-level clinical context |
| **[SIIM-ISIC 2020 (2020 data; 2021 descriptor)](https://www.nature.com/articles/s41597-021-00815-z)** **[[data]](https://challenge2020.isic-archive.com/)** | 33,126 images; 2,056 patients | 2 | Site, age, sex, patient context | Dermoscopic | CC BY-NC 4.0 | Patient-centric melanoma challenge |
| **[Fitzpatrick17k (2021)](https://arxiv.org/abs/2104.09957)** **[[data]](https://github.com/mattgroh/fitzpatrick17k)** | 16,577 images | 114 conditions | FST, diagnosis | Clinical | Source-dependent; see repository | Broad condition coverage assembled from two atlases |
| **[DDI (2022)](https://www.science.org/doi/10.1126/sciadv.abq6147)** **[[data]](https://ddi-dataset.github.io/)** | 656 images; 570 patients | 78 diagnoses; benign/malignant benchmark | FST, age, sex, pathology | Clinical | Research Use Agreement | Biopsy-confirmed, diverse-skin-tone evaluation dataset |
| **[HIBA (2023)](https://www.nature.com/articles/s41597-023-02630-0)** **[[data]](https://doi.org/10.34970/587329)** | 1,616 images (1,270 dermoscopic; 346 clinical) | 10 | Age, sex, FST, site, melanoma history, confirmation method | Dermoscopic + clinical | CC BY 4.0 | Argentinian/Hispanic American population |
| **[PROVe-AI (2023)](https://www.nature.com/articles/s41746-023-00872-1)** **[[data]](https://api.isic-archive.com/doi/prove-ai/)** | 603 lesions | Melanoma 95; non-melanoma 508 | Age, sex, site, FST, nevus phenotype, history | Dermoscopic | CC0 on official ISIC record | Prospective, biopsy-confirmed suspicious lesions |
| **[PASSION (2024)](https://arxiv.org/abs/2411.04584)** **[[data]](https://passionderm.github.io/#Dataset)** | 4,901 images | Multiple conditions | FST III-VI | Clinical | Custom PASSION license; redistribution restricted | Sub-Saharan African population |
| **[SCIN (2024)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11579799/)** **[[data]](https://github.com/google-research-datasets/scin)** | 10,408 images; 5,033 contributions | 419 SNOMED-CT categories | Self/estimated FST, Monk tone, symptoms, demographics | Smartphone clinical | Custom SCIN license | Crowdsourced, consented, mostly short-duration conditions |
| **[SLICE-3D / ISIC 2024 (2024)](https://www.nature.com/articles/s41597-024-03743-w)** **[[data]](https://challenge2024.isic-archive.com/)** | Train 401,059; test about 500,000 | Binary | 3D location, demographics | 3D-TBP crops | Mixed CC BY-NC / CC BY records | 15 mm × 15 mm lesion crops; classification rather than mask segmentation |
| **[DERM12345 (2024)](https://www.nature.com/articles/s41597-024-04104-3)** **[[data]](https://doi.org/10.7910/DVN/DAXZ7P)** | 12,345 images; 1,627 patients | 40 subclasses in a 3-level hierarchy | Patient ID, split, modality, taxonomy | Dermoscopic | CC BY 4.0 | Detailed hierarchical taxonomy from Türkiye |
| **[BCN20000 (2024 descriptor)](https://www.nature.com/articles/s41597-024-03387-w)** **[[data]](https://api.isic-archive.com/collections/249/)** | 18,946 images | 8 classes | Age, sex, site, date | Dermoscopic | CC BY 4.0 on collection | “Lesions in the wild,” including nails and mucosa |
| **[Mpox Skin Lesion v2.0 (2024 data version; preprint 2023)](https://arxiv.org/abs/2306.14169)** **[[data]](https://www.kaggle.com/datasets/joydippaul/mpox-skin-lesion-dataset-version-20-msld-v20)** | 755 images | 6 | Patient ID, validation status | Clinical | CC BY 4.0 on data page | Infectious-disease differential rather than pigmented-lesion focus |
| **[DDI-2 (2024 release; 2025 issue)](https://doi.org/10.1016/j.jid.2024.09.018)** **[[data]](https://daneshjoulab.github.io/ddi2-dataset/)** | 665 images; 550 patients | 169 diagnoses | FST, sub-ethnicity, site, pathology, workflow artifacts | Clinical | Registration + non-commercial Research Use Agreement | Biopsy-proven cohort of self-identified Asian patients |
| **[BALD (2024 data; 2025 issue)](https://doi.org/10.1016/j.jid.2024.12.021)** **[[data]](https://api.isic-archive.com/doi/braaff-annotated-acral-lesions-dataset-bald/)** | 666 images | Acral melanoma and nevi | BRAAFF dermoscopic pattern annotations | Dermoscopic | CC BY-NC | Multi-source acral-lesion set |
| **[DermaCon-IN (2025)](https://arxiv.org/abs/2506.06099)** **[[data]](https://doi.org/10.7910/DVN/W7OUZM)** | 5,450+ images; about 3,000 patients | 240+ diagnoses | Site, descriptors, FST, Monk tone, age, sex, certainty, hierarchy | Clinical | CC BY-NC-SA 4.0 | South Indian outpatient population |
| **[SkinDisNet (2025)](https://doi.org/10.1016/j.dib.2025.112239)** **[[data]](https://doi.org/10.17632/yj3md44hxg.2)** | 1,710 preprocessed images; 416 patients | 6 | Patient ID plus seven clinical/demographic attributes | Smartphone clinical | CC BY-NC 4.0 | Two-hospital Bangladesh cohort spanning inflammatory and infectious conditions; 11,970 augmented images are derivatives, not independent cases |
| **[ISIC-DICM-17K (2025)](https://openaccess.thecvf.com/content/CVPR2025W/MULA2025/html/Ahammed_Skin_Lesion_Classification_Using_Dermoscopic_Images_and_Clinical_Metadata_Insights_CVPRW_2025_paper.html)** **[[data]](https://api.isic-archive.com/doi/isic-dicm-17k/)** | 17,060 images; 9,188 specified lesions; 3,810 patients | 2 (melanoma, non-melanoma) | Age, sex, anatomic site | Dermoscopic | Mixed CC0 / CC BY / CC BY-NC upstream records | Balanced ISIC-derived benchmark; not an independent cohort |

### Specialized and access-limited classification collections

| Dataset | Scale | Scope | License / access | Why listed separately |
| --- | --- | --- | --- | --- |
| **[Dermofit Image Library](https://licensing.edinburgh-innovations.ed.ac.uk/product/dermofit-image-library)** | 1,300 images; 10 classes; binary masks | Standardized focal clinical images | Paid academic license (£75); institutional approval required; no commercial or educational use | Important legacy benchmark, but not an openly downloadable release |
| **[Consecutive Biopsies for Melanoma Across Year 2020 (2021 release)](https://api.isic-archive.com/doi/consecutive-biopsies-for-melanoma-across-year-2020/)** | 1,295 images | Consecutive MSKCC biopsy workflow with melanoma, nevus, lentigo, and related diagnoses | CC BY on official record | Narrow single-year clinical workflow rather than a general benchmark |
| **[15 Exemplar Infundibulocystic BCCs (2025)](https://api.isic-archive.com/doi/15-exemplar-infundibulocystic-basal-cell-carcinomas/)** | 15 images; 15 patients | Rare basal-cell-carcinoma subtype | CC BY | Exemplar teaching/research collection; too small for a general benchmark |
| **[MEL-SELF (2026)](https://api.isic-archive.com/collections/485/)** | 3,008 images; 837 lesions; 246 patients | Dermoscopic close-ups of benign and malignant lesions from the MEL-SELF trial | Public ISIC collection; no collection license or DOI shown—check image-level terms | Recent trial collection without a published dataset descriptor |

---

## 2. Segmentation and Detection Tasks

This section distinguishes pixel masks from bounding-box detection. Fixed lesion crops without masks, such as SLICE-3D, remain in classification.

| Dataset / task | Images | Annotation | Task | Modality | License / access | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| **[PH² (2013)](https://doi.org/10.1109/EMBC.2013.6610779)** **[[data]](https://www.fc.up.pt/addi/ph2%20database.html)** | 200; 29 with color masks | Binary lesion masks; six color masks for a subset | Segmentation | Dermoscopic | Research use | Expert masks |
| **[ISIC 2016 Task 1 (2016)](https://arxiv.org/abs/1605.01397)** **[[data]](https://challenge.isic-archive.com/landing/2016/37/)** | Train 900; test 379 | Binary masks | Segmentation | Dermoscopic | Check collection terms | Challenge masks |
| **[ISIC 2017 Task 1 (2017)](https://arxiv.org/abs/1710.05006)** **[[data]](https://challenge.isic-archive.com/landing/2017/42/)** | Train 2,000; validation 150; test 600 | Binary masks | Segmentation | Dermoscopic | Check collection terms | Expanded challenge set |
| **[ISIC 2018 Task 1 (2018)](https://arxiv.org/abs/1902.03368)** **[[data]](https://challenge.isic-archive.com/data/#2018)** | Train 2,594; validation 100; test 1,000 | Binary masks | Segmentation | Dermoscopic | Record-level ISIC terms vary | Previously missing from this catalog |
| **[iToBoS Detection (2025)](https://doi.org/10.1038/s41597-025-05483-x)** **[[data]](https://doi.org/10.6084/m9.figshare.28452545)** | Train 8,473; test 8,481 | Bounding boxes in YOLO and COCO formats | Detection | 3D-TBP tiles | CC BY 4.0 | Multiple lesions in natural skin-region tiles |
| **[IMA++ (2026 data release; 2025 preprint)](https://arxiv.org/abs/2512.21472)** **[[data]](https://api.isic-archive.com/collections/482/)** | 17,684 masks over 14,967 images | Expert and multi-annotator masks | Segmentation / disagreement | Dermoscopic | Underlying image terms vary | 2-5 masks for 2,394 images |
| **[ISIC 2018 Novice Segmentation Masks (2026)](https://api.isic-archive.com/doi/isic-2018-novice-segmentation-masks/)** **[[data]](https://api.isic-archive.com/doi/isic-2018-novice-segmentation-masks/)** | 11,720 masks | Manually reviewed novice masks | Segmentation / annotation bias | Dermoscopic | CC BY-NC | Released 2026-06-30 |

---

## 3. Dermoscopic Feature and Concept Annotations

| Dataset | Images | Features / concepts | Modality | License / access | Notes |
| --- | --- | --- | --- | --- | --- |
| **[PH² (2013)](https://doi.org/10.1109/EMBC.2013.6610779)** **[[data]](https://www.fc.up.pt/addi/ph2%20database.html)** | 200 | Pigment network, dots/globules, streaks, regression, blue-whitish veil, colors, asymmetry | Dermoscopic | Research use | P = present, A = absent, T = typical, AT = atypical |
| **[ISIC 2016 Task 2 (2016)](https://arxiv.org/abs/1605.01397)** **[[data]](https://challenge.isic-archive.com/landing/2016/38/)** | Train 807; test 335 | Globules and streaks at superpixel level | Dermoscopic | Check collection terms | SLIC superpixels |
| **[ISIC 2017 Part 2 (2017)](https://arxiv.org/abs/1710.05006)** **[[data]](https://challenge.isic-archive.com/landing/2017/43/)** | Train 2,000; validation 150; test 600 | Pigment network, negative network, streaks, milia-like cysts | Dermoscopic | Check collection terms | Superpixel annotations |
| **[ISIC 2018 Task 2 (2018)](https://doi.org/10.1038/sdata.2018.161)** **[[data]](https://challenge.isic-archive.com/landing/2018/46/)** | 2,594 | 2017 features plus globules | Dermoscopic | Check collection terms | Expanded feature set |
| **[Derm7pt (2019 issue; online 2018)](https://doi.org/10.1109/JBHI.2018.2824327)** **[[data]](https://derm.cs.sfu.ca/Welcome.html)** | 1,011 cases | Seven-point checklist, diagnosis, difficulty, elevation, site, sex | Clinical + dermoscopic | Research use; check site terms | Paired imaging |
| **[SkinCon (2022)](https://papers.nips.cc/paper_files/paper/2022/file/7318b51b52078e3af28197e725f5068a-Paper-Datasets_and_Benchmarks.pdf)** **[[data]](https://skincon-dataset.github.io/)** | 3,230 Fitzpatrick17k + 656 DDI images annotated | 48 clinical concepts | Clinical | Annotation release; upstream image terms apply | Older omission; enables concept prediction and interpretability |
| **[MSKCC Skin Tone Labeling (2024)](https://api.isic-archive.com/doi/mskcc-skin-tone-labeling-dataset/)** **[[data]](https://api.isic-archive.com/doi/mskcc-skin-tone-labeling-dataset/)** | 4,879 images; 1,257 lesions; 64 patients | FST, Monk, Pantone, colorimeter labels | Dermoscopic | CC BY | Prospective 2023-2024 skin-tone measurement study |

---

## 4. Temporal Datasets

Temporal resources contain repeated observations or longitudinal collection suitable for change analysis. Restricted PanDerm evaluation cohorts are listed separately so they are not confused with public releases.

| Dataset | Participants / images | Temporal characteristics | Modality | Key metadata | License / access | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| **[Repeated Dermoscopic Images / SDDI1 (2023 release)](https://doi.org/10.1111/jdv.19777)** **[[data]](https://api.isic-archive.com/doi/repeated-dermoscopic-images-of-melanocytic-lesions/)** | 66 patients; 585 images; 116 lesions | Five sequential acquisitions; one-year follow-up where available | Dermoscopic | Diagnosis and repeated-image identity | CC BY-NC on collection | Corrects the former ISIC-2017 citation and unsupported three-month claim |
| **[OHSU MoleMapper (2025)](https://doi.org/10.1038/s41597-025-05552-1)** **[[data]](https://www.synapse.org/Synapse:syn51520810)** | 27,499 mole images; 7,305 nearby-skin patches; 1,000 context images | Consumer smartphone collection from 2016-2022 | Clinical smartphone | Basic participant metadata | Qualified-researcher Synapse access | Six years of user-captured pigmented-lesion imagery; images are unlabeled |
| **[UQ Longitudinal (2025)](https://doi.org/10.1038/s41597-025-05880-2)** **[[data]](https://doi.org/10.48610/a13deaf)** | 480 participants; 250,162 tiles; 35,909 dermoscopic images | 340 participants with 2-7 timepoints; about six-month intervals; 2-3 years | 3D-TBP + dermoscopic | Demographics, site, nevus count, phenotype, ancestry, exposure/history | CC BY-NC-ND 4.0 | 9,389 unique lesions, including 30 melanomas |

### Restricted temporal evaluation cohorts

| Dataset | Source | Scope | Access status | Date note |
| --- | --- | --- | --- | --- |
| **SDDI2 (Vienna)** | [PanDerm](https://doi.org/10.1038/s41591-025-03747-y) | 229 sequential lesions; 458 images; paired short-term monitoring | Private / restricted | 2025 is PanDerm publication, not a public dataset release |
| **SDDI_Alfred** | [Source study](https://arxiv.org/abs/2110.05976) and [PanDerm](https://doi.org/10.1038/s41591-025-03747-y) | 122 patients; 730 images; 179 serial sequences collected 2007-2019 | Private / restricted | Source study published 2021; reused by PanDerm in 2025 |

---

## 5. Vision-Language Datasets

| Dataset | Image-text / VQA scale | Text annotation | Key metadata | Modality | License / access | Notable features |
| --- | --- | --- | --- | --- | --- | --- |
| **[SkinCAP (2024)](https://arxiv.org/abs/2405.18004)** **[[data]](https://huggingface.co/datasets/joshuachou/SkinCAP)** | About 4,000 pairs | Bilingual medical captions | FST, 178 diseases, 48 concepts, age, sex | Clinical | CC BY-NC-SA 4.0 | Derived from Fitzpatrick17k and DDI images |
| **[DermaVQA (2024)](https://doi.org/10.1007/978-3-031-72086-4_20)** **[[data]](https://osf.io/72rp3/overview)** | About 3,500 VQA pairs | English, Chinese, and Spanish VQA | Age, sex, diagnosis, treatment, author rank | Clinical | CC BY 4.0 on OSF project; source-content rights may vary | Consumer questions with professional responses |
| **[DermaSynth (2025)](https://arxiv.org/abs/2502.00196)** **[[data]](https://github.com/abdurrahimyilmaz/DermaSynth)** | 92,020 synthetic pairs from 45,205 images | Synthetic self-instruct VQA | Diagnosis, age, sex, site, skin type, symptoms | Clinical + dermoscopic | CC BY-NC 4.0 | Derived from DERM12345, BCN20000, PAD-UFES-20, SCIN, and HIBA |
| **[Derm1M (2025)](https://arxiv.org/abs/2503.14911)** **[[data]](https://github.com/SiyuanYan1/Derm1M)** | 1,029,761 pairs | Captions, hierarchy, concept labels | 390+ conditions, 130 concepts, history, symptoms, site, demographics, tone | Clinical + dermoscopic + pathology | CC BY-NC 4.0 on release | Aggregated educational and public sources; provenance matters |
| **[MM-Skin (2025)](https://arxiv.org/abs/2505.06152)** **[[data]](https://github.com/ZwQ803/MM-Skin)** | About 10,000 pairs + 27,000 VQA | Captions, VQA, instructions | Age, sex, demographics | Clinical + dermoscopic + pathology | Research use | Textbook-derived subsets |

---

## 6. Paired Multimodal Datasets

These resources intentionally pair clinical close-up and dermoscopic images, often with patient or lesion metadata. Some also appear in classification because they support both tasks.

| Dataset | Images / lesions / patients | Paired modalities and metadata | License / access | Notable features |
| --- | --- | --- | --- | --- |
| **[Derm7pt (2019 issue; online 2018)](https://doi.org/10.1109/JBHI.2018.2824327)** **[[data]](https://derm.cs.sfu.ca/Welcome.html)** | 1,011 lesion cases | Clinical + dermoscopic + seven-point checklist and demographics | Research use; check site terms | Same-lesion image pairs |
| **[HIBA (2023)](https://www.nature.com/articles/s41597-023-02630-0)** **[[data]](https://doi.org/10.34970/587329)** | 1,616 images | Dermoscopic + clinical + demographics/history | CC BY 4.0 | Argentinian cohort |
| **[MRA-MIDAS (2024 data; 2025 paper)](https://doi.org/10.1056/AIdbp2400732)** **[[data]](https://aimi.stanford.edu/datasets/mra-midas-Multimodal-Image-Dataset-for-AI-based-Skin-Cancer)** | 3,830 images; 1,290 lesions; 796 patients | Dermoscopic + 15/30 cm clinical images + patient/lesion metadata | Redivis account/subscription workflow; landing page does not state a license—verify current terms | Prospective Stanford/Cleveland Clinic cohort with extensive pathology confirmation; [public preprint](https://doi.org/10.1101/2024.06.27.24309562) |
| **[MILK10k (2025 data; 2026 issue)](https://doi.org/10.1016/j.jid.2025.06.1594)** **[[data]](https://api.isic-archive.com/doi/milk10k/)** | 10,480 images; 5,240 lesions | Paired clinical close-up + dermoscopic + age, sex, site, tone, diagnosis | CC BY-NC | 11 broad categories; 95.7% biopsied or excised |
| **[MCR-SL (2025)](https://www.mdpi.com/2306-5729/10/10/166)** **[[data]](https://doi.org/10.5281/zenodo.17306338)** | 2,131 images; 240 lesions; 60 subjects | 779 clinical + 1,352 dermoscopic images; rich subject/lesion/diagnosis metadata | CC BY 4.0 | Four-dermatologist panel; histopathology for 29 excised lesions |
| **[Actinic Keratosis Dermoscopy + HFUS (2026)](https://doi.org/10.1016/j.cmpb.2026.109364)** **[[data]](https://doi.org/10.17632/w3x8p3bf42.3)** | 222 paired observations; 74 patients | Dermoscopic + 20 MHz high-frequency ultrasound; age, sex, patient/marker IDs, AK stage | CC BY 4.0 | Healthy skin and AK grades 1-3; two-dermatologist staging |

---

## 7. Skin-Tone and Fairness Resources

This view highlights resources designed for population representation or tone annotation. It does not imply that tone labels are interchangeable: Fitzpatrick type, Monk tone, Pantone labels, and objective colorimetry measure different constructs.

| Dataset | Scale | Population / annotation focus | License / access | Primary use |
| --- | --- | --- | --- | --- |
| **[DDI (2022)](https://www.science.org/doi/10.1126/sciadv.abq6147)** **[[data]](https://ddi-dataset.github.io/)** | 656 images; 570 patients | FST I-VI; pathology-confirmed diagnoses | Research Use Agreement | Performance and bias evaluation across skin tones |
| **[DDI-2 (2024 release; 2025 issue)](https://doi.org/10.1016/j.jid.2024.09.018)** **[[data]](https://daneshjoulab.github.io/ddi2-dataset/)** | 665 images; 550 patients | Self-identified Asian patients; FST and sub-ethnicity | Registration + non-commercial Research Use Agreement | Representation and robustness evaluation |
| **[MSKCC Skin Tone Labeling (2024)](https://api.isic-archive.com/doi/mskcc-skin-tone-labeling-dataset/)** **[[data]](https://api.isic-archive.com/doi/mskcc-skin-tone-labeling-dataset/)** | 4,879 images; 1,257 lesions; 64 patients | FST, Monk, Pantone, and colorimeter labels | CC BY | Comparing subjective and measured tone labels |

---

## 8. Dermatopathology Datasets

| Dataset | Scale | Labels / modality | License / access | Notable features |
| --- | --- | --- | --- | --- |
| **[TCGA-SKCM (2015 study; current IDC access)](https://doi.org/10.1016/j.cell.2015.05.044)** **[[data]](https://portal.imaging.datacommons.cancer.gov/collections/tcga_skcm/)** | 470 subjects | Slide microscopy with linked clinical and molecular data; cutaneous melanoma | Public NCI imaging under applicable NCI data-use terms; linked molecular data may be open or controlled | Primarily metastatic melanoma; IDC also exposes derived annotations and segmentations |
| **[PATCH16 (2022)](https://pmc.ncbi.nlm.nih.gov/articles/PMC9723465/)** **[[data]](https://doi.org/10.11588/data/7QCR8S)** | 129,364 histological-slide patches from 386 cases | 16 histopathology classes | Check repository record terms | Older omission; patch-level dermatopathology benchmark |
| **[PUMA (2025)](https://doi.org/10.1093/gigascience/giaf011)** **[[data]](https://doi.org/10.5281/zenodo.15050523)** | 206 public training ROIs; paper/challenge cohort 310 ROIs | H&E melanoma nuclei and tissue instance/panoptic annotations | CC0 1.0 on Zenodo | Primary and metastatic melanoma; expert-reviewed nuclei and tissue labels plus context ROIs |
| **[Histo-Seg (2025 issue; data v2)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11803237/)** **[[data]](https://doi.org/10.17632/vccj8mp2cg.2)** | 38 whole-slide images from 14 participants | 12-class masks for skin layers, tissues, and carcinomas | Repository says CC BY 4.0; paper says non-commercial research only—resolve before commercial use | Histopathologist-annotated BCC, SCC, and intraepidermal carcinoma regions |
| **[DermpathNet (2026)](https://www.nature.com/articles/s41597-026-06715-4)** **[[data]](https://doi.org/10.5281/zenodo.17288670)** | 7,772 images | 166 diagnoses; dermatopathology figures | Source/image-specific licenses apply | Board-certified review; curated from openly accessible literature |

---

## Access and licensing notes

- `Open article` and `public landing page` are not dataset licenses.
- `CC BY`, `CC BY-NC`, `CC BY-NC-SA`, and `CC BY-NC-ND` have materially different reuse conditions; follow the exact linked version and attribution requirements.
- `Research Use Agreement`, `DUA`, `registration`, and `qualified researcher` indicate access conditions, not Creative Commons licenses.
- ISIC collections may combine records under different terms. Prefer the official collection or DOI page and check image-level terms when the collection says they vary.
- Derived datasets such as ISIC 2019, ISIC-DICM-17K, SkinCAP, DermaSynth, and Derm1M overlap or depend on upstream datasets. Do not sum their image counts as independent patient cohorts.
- `Private / restricted` resources are documented for completeness but are not publicly downloadable datasets.
- Legacy names such as SD-128/198/260 and atlas-derived image dumps are not presented as current releases when no stable, authoritative access record and reuse terms can be verified.
- Very small case supplements, synthetic-only corpora, and multi-source repackages are included only when they add a distinct task, annotation type, or access pathway.

## Contributing

Contributions and corrections are welcome. Please provide a primary paper or authoritative dataset record, canonical data link, release date, image/lesion/patient counts, modality and task, access status, exact license, and any derivation from existing datasets.

## Contact

Ping-Cheng Ku (pku1@jh.edu)

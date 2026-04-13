# awesome-oct

A curated list of open-source projects for **Optical Coherence Tomography (OCT)**, covering:

- Data parsing
- Annotation
- Deep learning segmentation
- Format conversion
- Visualization

> Goal: help researchers and engineers quickly find reusable OCT tooling.

---

## Table of Contents

- [Project List](#project-list)
- [How to Choose](#how-to-choose)
- [Recommended Workflow](#recommended-workflow)
- [Contributing](#contributing)

---

## Project List

| Category | Project | Description |
|---|---|---|
| Segmentation | [OCTDL](https://github.com/MikhailKulyabin/OCTDL) | Deep learning framework for OCT segmentation (training + inference) |
| Segmentation | [keras-UNET-OCT](https://github.com/SanderWooning/keras-UNET-OCT) | Lightweight UNet implementation in Keras |
| Segmentation | [OCT-Retinal-Layer-Segmenter](https://github.com/beasygo1ng/OCT-Retinal-Layer-Segmenter) | Retinal layer segmentation (ILM, RPE, etc.) |
| Segmentation | [eyeseg](https://github.com/MedVisBonn/eyeseg) | Advanced retinal layer and fluid segmentation |
| Annotation | [OCTAnnotate](https://github.com/krzyk87/OCTAnnotate) | OCT image annotation tool |
| Visualization | [eyelab](https://github.com/MedVisBonn/eyelab) | Interactive visualization and labeling UI |
| Data Parsing | [eyepy](https://github.com/MedVisBonn/eyepy) | Python library for Heidelberg `.e2e` data |
| Data Parsing | [heyexReader](https://github.com/ayl/heyexReader) | Low-level Heyex OCT reader |
| Data Parsing | [LibE2E](https://github.com/neurodial/LibE2E) | C++ E2E parser for production systems |
| Conversion | [OCT-Converter](https://github.com/marksgraham/OCT-Converter) | Convert OCT data to images / NumPy / DICOM |
| Conversion | [OCTA_DICOM2IMARIS](https://github.com/Henk-D/OCTA_DICOM2IMARIS) | Convert OCTA DICOM to Imaris format |

---

## How to Choose

### 1) Your goal is to read raw data
Start with: `eyepy`, `heyexReader`, `LibE2E`.

### 2) Your goal is segmentation modeling
Start with: `OCTDL`, `keras-UNET-OCT`, `eyeseg`.

### 3) Your goal is annotation and quality review
Start with: `OCTAnnotate`, `eyelab`.

### 4) Your goal is format interoperability for downstream analysis
Start with: `OCT-Converter`, `OCTA_DICOM2IMARIS`.

---

## Recommended Workflow

1. **Parse source data** with `eyepy` / `heyexReader` / `LibE2E`.
2. **Convert into common formats** with `OCT-Converter` (images or NumPy arrays).
3. **Annotate training sets** with `OCTAnnotate` or `eyelab`.
4. **Train and run inference** with `OCTDL` / `keras-UNET-OCT` / `eyeseg`.
5. **Visualize and review outputs** with `eyelab`.

---

## Contributing

PRs are welcome. Please include:

- Project link (GitHub)
- Category (Segmentation / Annotation / Data Parsing / Conversion / Visualization)
- One-sentence summary (feature, use case, or highlight)

If you want to add a new category, include a short rationale in your PR.

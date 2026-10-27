# awesome-oct

A curated list of open-source projects for **Optical Coherence Tomography (OCT)**, covering data acquisition, parsing, annotation, segmentation, conversion, and visualization workflows used in ophthalmology and retinal research.

> Goal: help researchers, clinicians, and engineers quickly discover reusable OCT tooling and choose the right components for their workflow.

---

## Why this repository exists

OCT data is rich but fragmented. Different devices, vendors, and file formats often require distinct tooling for:

- reading proprietary raw data
- converting data into a standard format
- annotating layers and lesions
- training or running segmentation models
- reviewing results visually

This repository brings together practical, open-source projects that address these steps and helps users navigate the ecosystem without reinventing common infrastructure.

---

## Scope

This list focuses on open-source tools relevant to OCT research and clinical workflows, especially for:

- retinal OCT and OCTA
- layer segmentation and fluid detection
- annotation and review interfaces
- vendor data parsing (e.g., Heidelberg `.e2e`)
- conversion to image, NumPy, or DICOM-oriented workflows
- visualization and labeling for analysis pipelines

It is intentionally practical and research-oriented rather than a comprehensive list of every OCT-related paper, package, or commercial product.

---

## Table of Contents

- [Project List](#project-list)
- [How to Choose](#how-to-choose)
- [Recommended Workflow](#recommended-workflow)
- [Common OCT Tasks](#common-oct-tasks)
- [Contributing](#contributing)

---

## Project List

| Category | Project | Description |
|---|---|---|
| Segmentation | [OCTDL](https://github.com/MikhailKulyabin/OCTDL) | Deep learning framework for OCT segmentation, covering training and inference workflows. |
| Segmentation | [keras-UNET-OCT](https://github.com/SanderWooning/keras-UNET-OCT) | Lightweight U-Net implementation in Keras for OCT image segmentation tasks. |
| Segmentation | [OCT-Retinal-Layer-Segmenter](https://github.com/beasygo1ng/OCT-Retinal-Layer-Segmenter) | Retinal layer segmentation tool focused on structures such as ILM and RPE. |
| Segmentation | [eyeseg](https://github.com/MedVisBonn/eyeseg) | Advanced retinal layer and fluid segmentation framework for OCT data. |
| Annotation | [OCTAnnotate](https://github.com/krzyk87/OCTAnnotate) | Annotation tool for labeling OCT images and regions of interest. |
| Visualization | [eyelab](https://github.com/MedVisBonn/eyelab) | Interactive visualization and labeling UI for OCT datasets and analysis outputs. |
| Data Parsing | [eyepy](https://github.com/MedVisBonn/eyepy) | Python library for reading Heidelberg `.e2e` OCT data. |
| Data Parsing | [heyexReader](https://github.com/ayl/heyexReader) | Low-level reader for Heyex OCT raw data. |
| Data Parsing | [LibE2E](https://github.com/neurodial/LibE2E) | C++ parser for E2E file formats used in production OCT pipelines. |
| Conversion | [OCT-Converter](https://github.com/marksgraham/OCT-Converter) | Converts OCT data into images, NumPy arrays, or other downstream-friendly formats. |
| Conversion | [OCTA_DICOM2IMARIS](https://github.com/Henk-D/OCTA_DICOM2IMARIS) | Converts OCTA DICOM data to Imaris-compatible format. |

---

## How to Choose

### 1) Your goal is to read raw OCT data

Start with: `eyepy`, `heyexReader`, `LibE2E`.

These projects help you open vendor-specific byte streams or data containers and transform them into a workable internal representation.

### 2) Your goal is segmentation modeling

Start with: `OCTDL`, `keras-UNET-OCT`, `eyeseg`.

These are useful when you want to detect retinal layers, subretinal fluid, or other clinically relevant biomarkers.

### 3) Your goal is annotation and review

Start with: `OCTAnnotate`, `eyelab`.

These tools help with manual labeling, quality inspection, and collaborative review of OCT scans.

### 4) Your goal is interoperability and downstream analysis

Start with: `OCT-Converter`, `OCTA_DICOM2IMARIS`.

These are especially useful when you need to bridge vendor-specific data with common file formats, analysis pipelines, or visualization tools.

---

## Recommended Workflow

A typical OCT project pipeline looks like this:

1. **Parse source data** with `eyepy`, `heyexReader`, or `LibE2E`.
2. **Normalize and convert** the data with `OCT-Converter` or a DICOM conversion workflow.
3. **Annotate the dataset** with `OCTAnnotate` or `eyelab`.
4. **Train or run segmentation models** with `OCTDL`, `keras-UNET-OCT`, or `eyeseg`.
5. **Visualize and review outputs** with `eyelab` or a custom analysis stack.

This order is a good default when building a research or prototype pipeline from raw OCT acquisitions to model outputs.

---

## Common OCT Tasks

### Data loading

If the challenge is opening raw formats or vendor files, the best starting point is a parser project such as `eyepy` or `LibE2E`.

### Model development

If the task is training a segmentation network, look at `OCTDL` or `keras-UNET-OCT` and evaluate whether you need a more specialized retinal segmentation framework like `eyeseg`.

### Review and QA

If the goal is checking model predictions or labeling difficult cases, use `OCTAnnotate` or `eyelab` to create a human-friendly review loop.

### Clinical interoperability

If the output needs to move between systems or be stored in DICOM-friendly forms, consider conversion tools such as `OCT-Converter` and `OCTA_DICOM2IMARIS`.

---

## Contributing

PRs are welcome. Please include:

- project link (GitHub)
- category (Segmentation / Annotation / Data Parsing / Conversion / Visualization)
- one-sentence summary describing the feature, use case, or highlight
- a brief note on whether it is vendor-specific, research-focused, or general-purpose

If you want to add a new category, include a short rationale in your PR.

### Contribution checklist

Before submitting a new project, make sure it is:

- relevant to OCT or OCTA workflows
- open-source and publicly accessible
- useful for real analysis, annotation, parsing, or visualization tasks
- sufficiently documented for other users to evaluate it quickly

---

## Notes

This repository is meant to be a practical pointer list rather than a formal benchmark or review publication. Project quality, maintenance status, and fit for a specific problem can vary, so it is recommended to check the linked repositories and documentation before adopting them in a production or clinical workflow.

---

## License

This repository is a curated directory and does not impose a software license on the projects it links to. Please refer to each linked project for its own licensing terms.

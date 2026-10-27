# awesome-oct

<p align="center">
  <img src="https://img.shields.io/badge/OCT-Optical%20Coherence%20Tomography-1f77b4?style=for-the-badge" alt="OCT" />
  <img src="https://img.shields.io/badge/Scope-Research%20%26%20Clinical%20Tools-28a745?style=for-the-badge" alt="Scope" />
  <img src="https://img.shields.io/badge/Status-Curated%20Open%20Source-ff7f0e?style=for-the-badge" alt="Status" />
</p>

A curated list of open-source projects for **Optical Coherence Tomography (OCT)**, covering data parsing, annotation, segmentation, conversion, and visualization workflows used in retinal imaging and OCT research.

> Goal: help researchers, clinicians, and engineers quickly discover the most relevant OCT tooling and choose the right tools for each stage of the pipeline.

---

## Overview

OCT imaging produces rich volumetric data, but real-world workflows are often fragmented across vendor-specific formats, analysis libraries, annotation tools, and segmentation pipelines. This repository brings together open-source projects that help with the full lifecycle of OCT analysis:

- reading proprietary data files
- converting formats into common representations
- annotating retinal structures and pathologies
- training or running segmentation models
- reviewing results and preparing data for downstream analysis

Whether you are building a research pipeline or exploring OCT tooling for clinical applications, this list is intended to be a practical starting point rather than an exhaustive benchmark.

---

## Scope

This list focuses on open-source tools relevant to OCT and OCTA workflows, especially for:

- retinal layer segmentation
- lesion and fluid detection
- annotation and quality review
- vendor-specific data access
- interoperability with DICOM, NumPy, or image-based pipelines
- visualization and manual inspection

---

## Project Categories

- [Data Parsing](#data-parsing)
- [Segmentation](#segmentation)
- [Annotation](#annotation)
- [Visualization](#visualization)
- [Conversion](#conversion)

---

## Project List

### Data Parsing

| Project | Description |
|---|---|
| [eyepy](https://github.com/MedVisBonn/eyepy) | Python library for reading Heidelberg `.e2e` OCT data. |
| [heyexReader](https://github.com/ayl/heyexReader) | Low-level reader for Heyex OCT data. |
| [LibE2E](https://github.com/neurodial/LibE2E) | C++ parser for E2E files used in OCT production pipelines. |

### Segmentation

| Project | Description |
|---|---|
| [OCTDL](https://github.com/MikhailKulyabin/OCTDL) | Deep learning framework for OCT segmentation, covering training and inference. |
| [keras-UNET-OCT](https://github.com/SanderWooning/keras-UNET-OCT) | Lightweight U-Net implementation in Keras for OCT image segmentation. |
| [OCT-Retinal-Layer-Segmenter](https://github.com/beasygo1ng/OCT-Retinal-Layer-Segmenter) | Retinal layer segmentation tool focused on structures such as ILM and RPE. |
| [eyeseg](https://github.com/MedVisBonn/eyeseg) | Advanced retinal layer and fluid segmentation framework. |

### Annotation

| Project | Description |
|---|---|
| [OCTAnnotate](https://github.com/krzyk87/OCTAnnotate) | Tool for labeling OCT images and regions of interest. |

### Visualization

| Project | Description |
|---|---|
| [eyelab](https://github.com/MedVisBonn/eyelab) | Interactive visualization and labeling UI for OCT datasets and results. |

### Conversion

| Project | Description |
|---|---|
| [OCT-Converter](https://github.com/marksgraham/OCT-Converter) | Converts OCT data into images, NumPy arrays, or other downstream-friendly formats. |
| [OCTA_DICOM2IMARIS](https://github.com/Henk-D/OCTA_DICOM2IMARIS) | Converts OCTA DICOM data to Imaris-compatible format. |

---

## How to Choose

### 1) You need to read raw vendor data

Start with:

- `eyepy`
- `heyexReader`
- `LibE2E`

These tools are the best entry point when your challenge is opening proprietary OCT files or translating them into a usable internal representation.

### 2) You want to build or run a segmentation model

Start with:

- `OCTDL`
- `keras-UNET-OCT`
- `eyeseg`

These projects are useful for retinal layer segmentation, fluid detection, and end-to-end OCT analysis workflows.

### 3) You need annotation or manual review

Start with:

- `OCTAnnotate`
- `eyelab`

These are good choices when you need human-in-the-loop labeling, dataset review, or quality inspection.

### 4) You care about interoperability and downstream pipelines

Start with:

- `OCT-Converter`
- `OCTA_DICOM2IMARIS`

These are especially valuable when your OCT data must be converted for broader scientific, imaging, or visualization workflows.

---

## Recommended Workflow

A typical OCT analysis pipeline looks like this:

1. Parse raw source data with `eyepy`, `heyexReader`, or `LibE2E`.
2. Normalize or convert the data with `OCT-Converter` or DICOM-oriented tooling.
3. Annotate training or validation sets using `OCTAnnotate` or `eyelab`.
4. Train or run segmentation models with `OCTDL`, `keras-UNET-OCT`, or `eyeseg`.
5. Visualize and review outputs with `eyelab` or custom analysis scripts.

This sequence is a good default for building an OCT research or prototype pipeline from acquisition to model output.

---

## Quick Picks by Use Case

| Need | Best Starting Point |
|---|---|
| Read vendor-specific OCT data | `eyepy`, `heyexReader`, `LibE2E` |
| Segment retinal layers or fluid | `OCTDL`, `keras-UNET-OCT`, `eyeseg` |
| Label or review scans | `OCTAnnotate`, `eyelab` |
| Convert data to another format | `OCT-Converter`, `OCTA_DICOM2IMARIS` |

---

## Contributing

Pull requests are welcome. To propose a new project, please include:

- project link (GitHub)
- relevant category
- 1-sentence summary describing the feature or use case
- any notes about vendor-specific support, clinical relevance, or research scope

If you want to add a new category, please include a short rationale in the PR.

### Contribution checklist

Before submitting a new project, make sure it is:

- relevant to OCT or OCTA workflows
- open-source and publicly accessible
- useful for parsing, annotation, visualization, model development, or conversion
- sufficiently documented so others can evaluate it quickly

---

## Notes

This repository is meant to be a practical index rather than a formal benchmark or review publication. Project quality, maintenance status, and fit for a specific use case can vary, so it is recommended to check each linked project’s documentation before adopting it in production or clinical work.

---

## License

This repository is a curated directory and does not impose a software license on the projects it links to. Please refer to each linked project for its own licensing terms.

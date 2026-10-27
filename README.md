# awesome-oct

A curated list of open-source projects for Optical Coherence Tomography (OCT).

This repository gathers useful OCT tools for data parsing, annotation, segmentation, conversion, and visualization.

## Categories

- [Data Parsing](#data-parsing)
- [Segmentation](#segmentation)
- [Annotation](#annotation)
- [Visualization](#visualization)
- [Conversion](#conversion)

## Data Parsing

- [eyepy](https://github.com/MedVisBonn/eyepy) — Python library for Heidelberg `.e2e` OCT data.
- [heyexReader](https://github.com/ayl/heyexReader) — Reader for Heyex OCT data.
- [LibE2E](https://github.com/neurodial/LibE2E) — C++ parser for E2E OCT files.

## Segmentation

- [OCTDL](https://github.com/MikhailKulyabin/OCTDL) — Deep learning framework for OCT segmentation.
- [keras-UNET-OCT](https://github.com/SanderWooning/keras-UNET-OCT) — Lightweight U-Net implementation in Keras.
- [OCT-Retinal-Layer-Segmenter](https://github.com/beasygo1ng/OCT-Retinal-Layer-Segmenter) — Retinal layer segmentation tool.
- [eyeseg](https://github.com/MedVisBonn/eyeseg) — Retinal layer and fluid segmentation framework.

## Annotation

- [OCTAnnotate](https://github.com/krzyk87/OCTAnnotate) — Annotation tool for OCT images and ROIs.

## Visualization

- [eyelab](https://github.com/MedVisBonn/eyelab) — Interactive visualization and labeling UI for OCT data.

## Conversion

- [OCT-Converter](https://github.com/marksgraham/OCT-Converter) — Convert OCT data into images, NumPy arrays, or other formats.
- [OCTA_DICOM2IMARIS](https://github.com/Henk-D/OCTA_DICOM2IMARIS) — Convert OCTA DICOM data to Imaris format.

## Quick Start by Goal

- Need to read raw OCT data? Start with `eyepy`, `heyexReader`, or `LibE2E`.
- Need segmentation models? Start with `OCTDL`, `keras-UNET-OCT`, or `eyeseg`.
- Need annotation or review? Start with `OCTAnnotate` or `eyelab`.
- Need format conversion? Start with `OCT-Converter` or `OCTA_DICOM2IMARIS`.

## Contributing

Contributions are welcome. Please submit a pull request with:

- project link
- category
- short description

This repository is a curated list and does not endorse any project as the only solution for every OCT workflow.

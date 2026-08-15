# Supplementary Table S1. Datasets, Computational Inputs, and Derived Modeling Resources

## Primary source dataset

### ACDC
ACDC served as the primary cardiac imaging source for the patient-specific
digital-twin cohort.

- Modality: cine cardiac MRI
- Inputs: expert ventricular/myocardial segmentation masks
- Patient-level information: de-identified subject ID, ED/ES phase,
  segmentation masks, available diagnostic category
- Processing:
  cohort selection → segmentation verification → 3D geometry reconstruction
  → FEM model generation
- DOI: 10.1109/TMI.2018.2837502
- Citation:
  Bernard O, et al. Deep Learning Techniques for Automatic MRI Cardiac
  Multi-Structures Segmentation and Diagnosis: Is the Problem Solved?
  IEEE Trans Med Imaging. 2018;37(11):2514-2525.

The original ACDC data are not redistributed in this repository.

## Reference datasets

### Sunnybrook Cardiac Data

Sunnybrook Cardiac Data were assessed as a reference cardiac imaging resource.
They are not treated as a source of the final five-patient FEM geometries unless
explicitly documented in the executed modeling record.

- DOI: 10.54294/g80ruo
- Source: Cardiac Atlas Project
- Citation:
  Radau P, et al. Cardiac MR Left Ventricle Segmentation Challenge.
  The MIDAS Journal. 2009.

The original dataset is not redistributed in this repository.

### CAMUS

CAMUS was retained as a reference/benchmark cardiac imaging resource and is not
treated as a source of the final five-patient CMR FEM geometries.

- Modality: 2D echocardiography
- DOI: 10.1109/TMI.2019.2900516
- Citation:
  Leclerc S, et al. Deep Learning for Segmentation Using an Open Large-Scale
  Dataset in 2D Echocardiography. IEEE Trans Med Imaging. 2019;38(9):2198-2210.

The original dataset is not redistributed in this repository.

## Study-derived computational artifacts

### Patient-specific derived geometry

Generated from verified source-dataset segmentations.

Processing:
surface reconstruction → surface QC → CAD/solid generation →
volumetric-domain generation.

### Finite-element mesh

Generated from the patient-specific computational geometry.

Processing:
coarse → medium → fine mesh generation → mesh-quality QC →
mesh-convergence assessment.

### Fiber-orientation field

Generated as a model-defined, literature-constrained myocardial fiber field.

Processing:
local myocardial coordinate construction → fiber assignment →
orientation/continuity QC.

All study-derived artifacts should be linked to the corresponding
patient/model identifier and execution record.

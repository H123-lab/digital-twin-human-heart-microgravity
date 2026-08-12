# Patient-Specific Digital Twin of the Human Heart Under Altered Gravity

## Overview

This repository contains the computational workflow, patient-specific input data records, geometry reconstruction documentation, finite-element model implementation, simulation design, execution records, verification procedures, and derived simulation results for the study:

**Patient-Specific Digital Twin Modeling of the Human Heart Under Altered Gravity Conditions**

The project investigates the mechanical response of patient-specific cardiac geometry under a controlled gravity sweep ranging from terrestrial gravity to microgravity.

The computational framework includes:

- patient-specific cardiac anatomy
- end-diastolic and end-systolic segmentation
- three-dimensional surface reconstruction
- CAD/solid geometry generation
- myocardial fiber-field construction
- nonlinear hyperelastic constitutive modeling
- finite-element discretization
- numerical verification
- baseline 1g simulation
- altered-gravity simulations
- fiber-orientation sensitivity analysis
- material-parameter sensitivity analysis
- basal boundary-condition sensitivity analysis
- pressure sensitivity analysis
- provenance and reproducibility auditing

---

## Study Workflow

The computational workflow is organized into the following phases:

### Phase I — Dataset and Cohort Preparation

Source datasets are screened and eligible subjects are selected according to the predefined study protocol.

### Phase II — Patient-Specific Digital Twin Construction

Patient-specific cardiac anatomy is reconstructed from segmentation masks and converted into computational geometry.

The workflow includes:

1. segmentation verification
2. surface reconstruction
3. surface quality control
4. CAD repair
5. volumetric-domain generation
6. myocardial fiber-field construction
7. constitutive model implementation
8. boundary-condition definition

### Stage 3 — Computational Verification and Simulation

Stage 3 contains:

- 3A: Geometry/Fiber/Material Verification
- 3B: FEM Discretization
- 3C: Numerical Verification
- 3D: Scientific Gravity Experiment
- 3E: Robustness and Sensitivity Analysis
- 3F: Final Audit and Reproducibility Verification

### Gravity Conditions

The primary gravity sweep consists of:

- 1.00g
- 0.75g
- 0.50g
- 0.38g
- 0.16g
- 0.00g

where effective gravitational acceleration is represented as:

g_eff = gamma × 9.81 m/s²

---

## Computational Framework

The finite-element simulations are implemented using COMSOL Multiphysics.

The model incorporates:

- geometrically nonlinear solid mechanics
- anisotropic myocardial material behavior
- patient-specific myocardial geometry
- model-derived myocardial fiber orientation
- cavity pressure loading
- basal constraints
- gravity-dependent body-force loading

The constitutive formulation and numerical parameters are documented in the corresponding model implementation and simulation parameter workbooks.

---

## Repository Organization

```text
01_Dataset_and_Cohort/
02_Input_Provenance/
03_Geometry_Reconstruction/
04_Digital_Twin_Construction/
05_COMSOL_Model/
06_Simulation_Design/
07_Simulation_Execution/
08_Simulation_Results/
09_Stage_3_Verification/
10_Methods_and_Supplementary/
11_Reproducibility_Artifacts/

Source Data and Data Governance
The original source imaging datasets are not redistributed in this repository. Source datasets remain subject to the access, licensing, and redistribution conditions established by their respective dataset providers. Only permitted derived cohort information, computational metadata, model specifications, execution records, and simulation outputs are provided. No directly identifying patient information is intentionally included.

Data Provenance
Patient-specific anatomical information is derived from the designated cardiac imaging datasets.
The repository distinguishes between:
dataset-derived information
mask-derived geometry
model-derived fiber orientation
literature-derived constitutive parameters
study-defined experimental conditions
computationally defined solver settings
simulation-derived outputs

Numerical Verification
The computational verification framework includes:
surface-volume agreement
surface topology checks
geometry integrity checks
fiber-field continuity checks
constitutive implementation verification
mesh-quality assessment
mesh-convergence analysis
nonlinear solver convergence
energy and numerical consistency checks.

Scientific Experiment
The primary experiment evaluates cardiac mechanical response across the predefined gravity conditions.
Primary output variables include:
maximum principal stress
von Mises stress
fiber-direction stress
maximum principal strain
fiber strain
displacement
LV cavity volume
myocardial volume
strain energy
Additional analyses include pressure-response and predefined sensitivity analyses.

Reproducibility
The repository is designed to preserve the computational chain from source cohort selection through patient-specific geometry reconstruction, model implementation, numerical verification, gravity simulation, sensitivity analysis, and final audit. Where distribution is permitted, computational artifacts such as COMSOL models, geometry files, meshes, solver logs, convergence records, exported numerical results, and checksums are retained in the reproducibility-artifact directory.

Important Interpretation
Simulation outputs are computational results and should not be interpreted as direct clinical measurements. Patient-specific anatomy is dataset-derived, whereas myocardial fiber orientation, constitutive parameters, boundary conditions, and altered-gravity conditions are model-defined or literature-constrained components of the computational experiment.

Software
Primary computational platform: COMSOL Multiphysics 6.4
Supporting analysis may include:
Python
NumPy
pandas
MATLAB or equivalent numerical analysis tools where applicable

Repository Status
This repository contains the documented computational workflow and associated research records for the digital-twin study. The final quantitative results reported in the manuscript should correspond exclusively to executed and archived computational outputs.

Citation
A formal citation record will be provided with the final manuscript and repository release.

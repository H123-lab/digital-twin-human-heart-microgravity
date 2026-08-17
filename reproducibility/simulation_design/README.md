# Computational Reproducibility Registry

This directory contains the structured computational evidence and reproducibility records associated with the five-patient patient-specific cardiac digital-twin gravity study.

## Cohort

Five patient-specific left-ventricular models were evaluated:

- P001
- P002
- P003
- P004
- P005

## Prespecified gravity design

The computational design contains six gravity conditions:

- 1.00 G
- 0.75 G
- 0.50 G
- 0.38 G
- 0.16 G
- 0.00 G

This corresponds to 30 prespecified patient–gravity conditions.

## Reproducibility records

The repository contains:

- patient–gravity simulation design
- geometry quality-control registry
- mesh registry
- mesh-convergence registry
- solver summary and native solver logs
- myocardial fiber-field definition
- sensitivity-analysis outputs
- gravity-resolved mechanical results
- 1 G versus 0 G summary results

## Evidence status

The structured files in this directory represent the computational evidence available for manuscript preparation and audit.

Native COMSOL master model files (.mph) and certain native field-export artifacts are not included unless explicitly recovered and released separately.

Reported mesh-convergence percentages should be considered registry-level evidence pending verification against native unrounded endpoint values.

The repository does not represent reconstructed or placeholder data as native solver exports.

## Units

Stress: kPa  
Strain: %  
Displacement: mm  
Volume: mL or cm³ where explicitly specified  
Strain energy: J  
Gravity: fraction of standard Earth gravity (G)

## Reproducibility principle

All manuscript numerical claims should be traceable to one of the structured result or quality-control files in this directory. Where native source recovery remains pending, the manuscript should state the limitation explicitly rather than infer or reconstruct unavailable native outputs.

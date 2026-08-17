# Computational Results Validation Status

## Purpose

This file records the reconciliation status of numerical and quality-control
records used for manuscript preparation.

The validation registry distinguishes between:

1. values directly documented in the available computational records;
2. values that can be cross-checked between structured datasets; and
3. values requiring verification against native COMSOL model files or
   unrounded native solver outputs.

## Current status

The five-patient gravity-results dataset and the 1 G versus 0 G summary are
internally organized around the same patient-specific gravity experiment.

The solver summary is supported by the corresponding patient-level solver
iteration records supplied for P001-P005.

Geometry and mesh quality-control records are maintained separately from
primary mechanical results.

## Native-source limitations

Native COMSOL `.mph` master model files are not included in this public
reproducibility directory.

Where a result depends on native unrounded solver endpoints, native field
exports, native coordinate definitions, or proprietary/internal model
implementation details, the repository does not represent reconstructed
values as native exports.

## Mesh convergence

The reported fine-versus-medium convergence percentages are retained as
documented registry values.

Native unrounded endpoint verification remains pending.

The reported criterion is:

fine-versus-medium difference <= 2%.

## Fiber field

The documented fiber construction uses model-defined endocardial and
epicardial fiber angles of +60 degrees and -60 degrees, respectively, with
continuous transmural interpolation.

The exact native implementation of the transmural coordinate, interpolation
equation, coordinate system, and spatial vector expression is not claimed to
be publicly reproduced unless recovered from the native model.

## Sensitivity analysis

Sensitivity outputs are retained as structured endpoint records.

Percentage changes should be interpreted as reported computational results
unless independently recomputed from verified native unrounded values.

## Public repository principle

The public repository contains structured reproducibility metadata,
quality-control summaries, selected numerical outputs, and documentation.

It does not require release of native COMSOL master model files or other
implementation artifacts that are not necessary for documenting the study.

No placeholder, reconstructed, or invented file is represented as a native
COMSOL export.

## Manuscript rule

Only numerical claims that are traceable to the structured repository
records should be used in the manuscript.

Where native-source verification remains unavailable, the manuscript will
use appropriately qualified language.

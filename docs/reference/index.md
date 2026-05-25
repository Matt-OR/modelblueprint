# Package index

## The ModelBlueprint class

The core S7 class that wraps a fitted model with its data, pipeline
functions, and metadata. All other functions in the package operate on
`ModelBlueprint` objects.

- [`ModelBlueprint`](https://github.com/matt/ModelBlueprint/reference/ModelBlueprint.md)
  : ModelBlueprint: a model-agnostic container for ML model lifecycles

## Predict

Generate predictions from a `ModelBlueprint`. Applies the full pipeline:
pre-processing → feature engineering → model prediction →
post-processing.

- [`predict(`*`<ModelBlueprint>`*`)`](https://github.com/matt/ModelBlueprint/reference/predict.ModelBlueprint.md)
  : Generate predictions from a ModelBlueprint

## Analysis plots

Core diagnostic plots. Each function works on a plain `data.frame` or
dispatches automatically from a `ModelBlueprint`, pulling the target,
exposure, and model from the object’s slots.

- [`one_way()`](https://github.com/matt/ModelBlueprint/reference/one_way.md)
  : Create a one-way analysis plot
- [`one_way(`*`<ModelBlueprint>`*`)`](https://github.com/matt/ModelBlueprint/reference/one_way.ModelBlueprint.md)
  : One-way analysis for a ModelBlueprint
- [`pdp()`](https://github.com/matt/ModelBlueprint/reference/pdp.md) :
  Partial dependence plot for any predict()-compatible model
- [`pdp(`*`<ModelBlueprint>`*`)`](https://github.com/matt/ModelBlueprint/reference/pdp.ModelBlueprint.md)
  : Partial dependence plot for a ModelBlueprint
- [`gain()`](https://github.com/matt/ModelBlueprint/reference/gain.md) :
  Cumulative Gains Chart
- [`gain(`*`<default>`*`)`](https://github.com/matt/ModelBlueprint/reference/gain.default.md)
  : Cumulative Gains Chart (default method)
- [`pred_vs_obs()`](https://github.com/matt/ModelBlueprint/reference/pred_vs_obs.md)
  : Predicted vs Observed Calibration Plot
- [`residuals_grouped()`](https://github.com/matt/ModelBlueprint/reference/residuals_grouped.md)
  : Grouped Residuals vs Predicted Plot
- [`sami()`](https://github.com/matt/ModelBlueprint/reference/sami.md) :
  SAMI Double Lift Chart

## Save and load

Persist a `ModelBlueprint` to disk and restore it in a later session.
Supports native R models and H2O models. Data slots saved as Feather
files for speed; factor levels are preserved exactly.

- [`saveMB()`](https://github.com/matt/ModelBlueprint/reference/saveMB.md)
  : Save a ModelBlueprint to disk
- [`loadMB()`](https://github.com/matt/ModelBlueprint/reference/loadMB.md)
  : Load a ModelBlueprint from disk

## Data manipulation

Pipe-friendly methods for filtering, mutating, and joining data within a
`ModelBlueprint`’s internal datasets. Each method returns a new
`ModelBlueprint` — the original is never mutated.

- [`filter(`*`<ModelBlueprint>`*`)`](https://github.com/matt/ModelBlueprint/reference/filter.ModelBlueprint.md)
  : Filter rows in a ModelBlueprint's datasets
- [`mutate(`*`<ModelBlueprint>`*`)`](https://github.com/matt/ModelBlueprint/reference/mutate.ModelBlueprint.md)
  : Mutate columns in a ModelBlueprint's datasets
- [`left_join(`*`<ModelBlueprint>`*`)`](https://github.com/matt/ModelBlueprint/reference/left_join.ModelBlueprint.md)
  : Left-join into a ModelBlueprint's datasets

## Utilities

Helper functions for data preparation.

- [`unitize()`](https://github.com/matt/ModelBlueprint/reference/unitize.md)
  : Unitize a numeric variable to the range 0 to 1

## Example ModelBlueprints

Ready-to-run `ModelBlueprint` constructors covering common R model
types. All use the built-in `mtcars` dataset. Useful for learning,
testing, and reproducing examples from the documentation.

- [`mb_lm_regression()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  [`mb_lm_classification()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  [`mb_glm_regression()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  [`mb_glm_binomial()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  [`mb_glm_poisson()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  [`mb_rpart_regression()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  [`mb_rpart_classification()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  [`mb_rf_regression()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  [`mb_rf_classification()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  [`mb_xgb_regression()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  [`mb_xgb_classification()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  [`mb_h2o_regression()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  [`mb_h2o_classification()`](https://github.com/matt/ModelBlueprint/reference/mb_examples.md)
  : Example ModelBlueprint objects

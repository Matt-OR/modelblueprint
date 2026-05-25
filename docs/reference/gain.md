# Cumulative Gains Chart

Plots cumulative gains curves for one or more competing scores against a
perfect model baseline. The Gini coefficient for each score is shown in
the legend.

## Usage

``` r
gain(data, ...)

# S3 method for class 'ModelBlueprint'
gain(
  data,
  set = c("train", "test", "holdout"),
  title = NULL,
  ret = c("plot", "data", "gini"),
  ...
)
```

## Arguments

- data:

  A `ModelBlueprint` object.

- ...:

  Passed to the default method.

- set:

  Which dataset to use: `"train"`, `"test"`, or `"holdout"`.

- title:

  Chart title. Defaults to `model_display_name`.

- ret:

  `"plot"`, `"data"`, or `"gini"`. Default `"plot"`.

## Value

A plotly object, list of data.tables, or list of Gini values.

## Examples

``` r
if (FALSE) { # \dontrun{
mb <- ModelBlueprint(
  model  = glm(vs ~ wt + hp, data = mtcars, family = binomial),
  train  = mtcars,
  y_name = "vs",
  model_display_name = "logistic_vs"
)
gain(mb)
} # }
```

# Mutate columns in a ModelBlueprint's datasets

Mutate columns in a ModelBlueprint's datasets

## Usage

``` r
# S3 method for class 'ModelBlueprint'
mutate(.data, ..., sets = c("train", "test", "holdout"))
```

## Arguments

- .data:

  A `ModelBlueprint`.

- ...:

  Expressions passed to
  [`dplyr::mutate()`](https://dplyr.tidyverse.org/reference/mutate.html).

- sets:

  Which datasets to mutate. Default: all non-NULL.

## Value

A new `ModelBlueprint`.

# Filter rows in a ModelBlueprint's datasets

Filter rows in a ModelBlueprint's datasets

## Usage

``` r
# S3 method for class 'ModelBlueprint'
filter(.data, ..., sets = c("train", "test", "holdout"))
```

## Arguments

- .data:

  A `ModelBlueprint`.

- ...:

  Filter expressions passed to
  [`dplyr::filter()`](https://dplyr.tidyverse.org/reference/filter.html).

- sets:

  Which datasets to filter. Default: all non-NULL.

## Value

A new `ModelBlueprint`.

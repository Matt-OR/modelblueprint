# Left-join into a ModelBlueprint's datasets

Left-join into a ModelBlueprint's datasets

## Usage

``` r
# S3 method for class 'ModelBlueprint'
left_join(x, y, by = NULL, ..., sets = c("train", "test", "holdout"))
```

## Arguments

- x:

  A `ModelBlueprint`.

- y:

  A `data.frame` to join.

- by:

  Join keys.

- ...:

  Passed to
  [`dplyr::left_join()`](https://dplyr.tidyverse.org/reference/mutate-joins.html).

- sets:

  Which datasets to join. Default: all non-NULL.

## Value

A new `ModelBlueprint`.

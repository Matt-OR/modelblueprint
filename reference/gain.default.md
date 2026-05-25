# Cumulative Gains Chart (default method)

Cumulative Gains Chart (default method)

## Usage

``` r
# Default S3 method
gain(
  data,
  pred = "predict",
  obs = NA_character_,
  exposure = "exposure",
  title = "Cumulative Gains",
  ret = c("plot", "data", "gini"),
  ...
)
```

## Arguments

- data:

  A `data.frame` or `data.table`.

- pred:

  `[character]` Name(s) of competing score columns.

- obs:

  `[character(1)]` Name of the target variable column.

- exposure:

  `[character(1)]` Name of the exposure column. Default `"exposure"`.

- title:

  `[character(1)]` Chart title.

- ret:

  `"plot"`, `"data"`, or `"gini"`. Default `"plot"`.

- ...:

  Unused.

## Value

A plotly object, list of data.tables, or list of Gini values.

## Examples

``` r
if (FALSE) { # \dontrun{
df <- data.frame(
  obs      = c(0, 1, 0, 1, 1),
  pred     = c(0.1, 0.9, 0.2, 0.8, 0.7),
  exposure = rep(1, 5)
)
gain(df, pred = "pred", obs = "obs", exposure = "exposure")
} # }
```

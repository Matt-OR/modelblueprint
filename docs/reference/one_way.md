# Create a one-way analysis plot

Bins a feature variable, computes exposure-weighted means of one or more
observed variables per bin, and returns a dual-axis plotly chart (bars =
exposure, lines = weighted means). Optionally splits by a second
variable.

## Usage

``` r
one_way(data, ...)

# Default S3 method
one_way(
  data,
  var,
  obs = "target",
  exposure = "exposure",
  split = NA_character_,
  bins = 35L,
  type_agg = c("equal_exposure", "equal_range"),
  ret = c("plot", "data"),
  ...
)
```

## Arguments

- data:

  A `data.frame` or `data.table`.

- ...:

  Arguments passed to methods.

- var:

  `[character(1)]` Column to plot on the x-axis.

- obs:

  `[character()]` One or more column names to summarise on the y-axis
  (right axis). Default `"target"`.

- exposure:

  `[character(1)]` Column of exposure weights. If the column does not
  exist in `data`, every row is given weight 1. Default `"exposure"`.

- split:

  `[character(1) | NA]` Optional column to split lines by. `NA`
  (default) produces a single set of lines.

- bins:

  `[integer(1)]` Number of equal-exposure bins for numeric variables
  with more than `bins` unique values. Default 35.

- type_agg:

  `[character(1)]` Binning strategy for numeric variables:
  `"equal_exposure"` (default) or `"equal_range"`.

- ret:

  `[character(1)]` `"plot"` (default) returns a plotly object; `"data"`
  returns the aggregated data.table.

## Value

A plotly object, or a data.table when `ret = "data"`, or `NULL` with a
warning if the plot cannot be produced.

## Examples

``` r
if (FALSE) { # \dontrun{
one_way(mtcars, var = "wt", obs = "mpg", bins = 10)
one_way(mtcars, var = "cyl", obs = c("mpg", "hp"), split = "am")
} # }
```

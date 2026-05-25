# Compute bin labels and midpoints for a feature vector

Returns a list with:

- `labels` : character vector (length = nrow of input), one label per
  row

- `midpoints` : named numeric vector, bin label -\> numeric midpoint (NA
  for categorical bins)

- `is_numeric`: logical, whether numeric binning was applied

## Usage

``` r
compute_bins(x, bins, type_agg)
```

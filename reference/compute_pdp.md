# Compute PDP values for each bin

For each bin, fixes the feature at its midpoint (numeric) or label
(categorical), runs predictions across the full sample, and returns the
mean prediction.

## Usage

``` r
compute_pdp(rep_set, var, model, bin_info, expo_col)
```

## Value

data.table with columns: .bin, pdp_mean

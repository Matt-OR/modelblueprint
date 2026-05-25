# Aggregate observed and in-sample predicted values per bin

Operates on `dt` which must already have columns `.bin`, `.pred`, the
obs column, and the exposure column.

## Usage

``` r
aggregate_pdp_oneway(dt, obs, expo_col)
```

## Value

data.table with columns: .bin, obs_mean, pred_mean, exposure

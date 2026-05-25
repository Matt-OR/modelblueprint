# Render the PDP chart

Produces a dual-axis plotly chart that exactly matches one_way()
styling:

- Left axis : yellow exposure bars

- Right axis : observed mean (purple), avg predicted (blue), PDP (teal)

- Global reference lines for both observed and predicted means

## Usage

``` r
plot_pdp(result, var, obs, model_name, global_obs, global_pred)
```

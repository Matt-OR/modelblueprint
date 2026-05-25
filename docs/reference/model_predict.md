# Dispatch prediction to the correct backend

Detects the model class and calls the appropriate prediction function:

- H2O models : converts newdata to an H2O frame, calls h2o.predict(),
  extracts the result back to R, then removes the temp frame

- All others : calls predict(model, newdata) via S3/S4 dispatch and
  coerces whatever shape is returned to a numeric vector

## Usage

``` r
model_predict(model, newdata)
```

## Arguments

- model:

  A fitted model object (any class).

- newdata:

  A data.table or data.frame of predictor values.

## Value

       A numeric vector of predictions, one per row of newdata.

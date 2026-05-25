# Generate predictions from a ModelBlueprint

Applies `pre_process_fun` -\> `feat_eng_fun` -\> model prediction -\>
`post_process_fun` to `newdata`.

## Usage

``` r
# S3 method for class 'ModelBlueprint'
predict(object, newdata, ...)
```

## Arguments

- object:

  A `ModelBlueprint`.

- newdata:

  A `data.frame` or `data.table`.

- ...:

  Unused.

## Value

A numeric vector of predictions.

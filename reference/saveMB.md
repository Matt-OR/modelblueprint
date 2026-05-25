# Save a ModelBlueprint to disk

Serialises a `ModelBlueprint` to a compressed `.tar.gz` archive
containing all components needed to fully reconstruct it: model, data
splits, pipeline functions, and metadata.

## Usage

``` r
saveMB(object, ...)
```

## Arguments

- object:

  A `ModelBlueprint` object.

- ...:

  Currently unused. Reserved for future subclass methods.

- path:

  Directory to write the archive to. Default: working directory.

- filename:

  Optional filename. When `NULL`, `model_display_name` is used.

## Value

Invisibly returns the full normalised path to the saved archive.

## See also

[`loadMB()`](https://matt-or.github.io/modelblueprint/reference/loadMB.md)

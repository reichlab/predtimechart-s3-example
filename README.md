# predtimechart-s3-example

This repo contains some initial investigations into how we might use the predtimechart component, pulling in data from an S3 bucket.  To do this, I copied over the repo for [Covid-19-Hub-Vizualization](https://github.com/reichlab/Covid-19-Hub-Vizualization) and made some light updates to `index.html`.

Current status: proof of concept of dynamically loading data from a single parquet file that lives in an S3 bucket into a duckdb-wasm database.

Next steps:
 - Figure out the best way to pull in multiple data files
 - Update initialization arguments for predtimechart to use values specific to this flu hub, ideally obtained by looking at contents of S3 bucket (in javascript, so this can be done dynamically at the time the site loads)
 - Update the `_fetchData` function to use these data, selecting relevant data and formatting in the target json structure

## To test

From this repo's root, run:

```
python -m http.server
```

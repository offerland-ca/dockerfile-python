# A Docker Image with `python`, `python-dev` and `gdal`

## Introduction

The official Python image does not include the `python-dev` package. Attempting to manually install this package can result in a broken image due to version mismatches between `python` and `python-dev`. To address this,
we have installed the necessary packages on top of the default Ubuntu images.

## How To

For creating new images you need to define a target and its dockerfile in `docker-bake.json`
as we did for `ubuntu-22.04` and then create a tag to trigger the workflow:

```bash
git tag ubuntu-22_04
```

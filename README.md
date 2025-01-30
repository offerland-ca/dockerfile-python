# A Docker Image with `python`, `python-dev` and `gdal`

## Introduction

The official Python image does not include the `python-dev` package. Attempting to manually install this package can result
in a broken image due to version mismatches between `python` and `python-dev`. To address this,
we have installed the necessary packages on top of the default Ubuntu images:

- Dockerfile.ubuntu-20.04
- Dockerfile.ubuntu-22.04
- Dockerfile.ubuntu-24.04

Our current need is having `gdal` library to be used by python and because of that you can install `libgdal-dev`
which doesn't have any dependency to `python-dev`.

- Dockerfile.3.11-gdal
- Dockerfile.3.12-gdal
- Dockerfile.3.13-gdal

## How To

For creating new images you need to define a target and its Dockerfile in `docker-bake.json`
as we did for `ubuntu-22.04` and then the target into the main target, so it runs by pushing on the main branch.

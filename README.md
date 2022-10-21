# Dcokerfile with python, python-dev and gdal

## Introduction

Official python image lacks the `python-dev` package and if you want to install it manually
it breaks the image becase the python version and python-dev version are different.
In the image we installed these packages on default images like _ubuntu_.

For creating new images you need to define a target and its dockerfile in `docker-bake.json`
as we did for `ubuntu-22.04` and then tag:

```bash
git tag ubuntu_22.04
```

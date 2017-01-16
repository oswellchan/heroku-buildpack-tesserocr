# Heroku Buildpack Tesserocr

This buildpack installs [tesserocr](https://github.com/sirfz/tesserocr) (Python wrapper for [Tesseract](https://github.com/tesseract-ocr/tesseract) API) and it's necessary dependencies.  

It includes:  

1. [tesserocr](https://github.com/sirfz/tesserocr) v2.1.3
2. [Tesseract](https://github.com/tesseract-ocr/tesseract) v3.04.01
3. [Cython](http://cython.org/) v0.25.2

## Configuration

Run the following commands for your app:

```
heroku buildpacks:set heroku/python
heroku buildpacks:add https://github.com/oswellchan/heroku-buildpack-tesserocr
```

It is important to set buildpack `heroku/python` as first so that the Python environment is available when the compile script installs the python packages.
   

## Note
This builds off the [fork](https://github.com/oswellchan/heroku-buildpack-tesseract) of [matteotiziano's heroku-buildpack-tesseract](https://github.com/matteotiziano/heroku-buildpack-tesseract).

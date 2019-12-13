# Source
This file is based on [github.com/mattfullerton/tika-tesseract-docker/](https://github.com/mattfullerton/tika-tesseract-docker/blob/master/README.md)

The Dockerfile has been modified to add norwegian language support for tesseract-ocr.

# Build and run
To build and run the container, do the following:

    sudo docker build -t tika-tesseract:1.23
    sudo docker run -d -p 9998:9998 tika-tesseract:1.23

To update to a newer version of tika, change the version in the Dockerfile and make sure the base address hasn't changed. Then build and tag with the newer version.

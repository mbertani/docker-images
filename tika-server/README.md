# Source
This file is based on [https://github.com/LogicalSpark/docker-tikaserver/blob/master/Dockerfile](https://github.com/LogicalSpark/docker-tikaserver/)

The Dockerfile has been modified to add norwegian language support for tesseract-ocr.

# Build and run
To build and run the container, do the following:

    sudo docker build -t tika-tesseract:1.23
    sudo docker run -d -p 9998:9998 tika-tesseract:1.23

To update to a newer version of tika, change the version in the Dockerfile and make sure the base address hasn't changed. Then build and tag with the newer version.

To test run:

    curl -T <your pdf file> http://localhost:9998/tika


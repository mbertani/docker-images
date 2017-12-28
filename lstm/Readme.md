# LSTM
Docker image to work with LSTM networks. 

## Features
- Uses image `continuumio/anaconda3:latest` as base image, with anaconda and python3
- Adds theano, tensorflow, kerans and jupyter
- Port 8888 for the jupyter server is exposed

## Setup
1. Assuming you are in the directory of the Dockerfile, run:

```
$ docker build -t lstm .
```

2. If the build process went OK, you can tag the image:

```
$ docker tag lstm mbertani/lstm:latest
```

3. Push the image to dockerhub.
```
$ docker login
$ docker push mbertani/lstm:latest
``` 

4. Test the image, for example by using port 9001 in you localhost:

```
$ docker run -p 9001:8888 mbertani/lstm:latest
```
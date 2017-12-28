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

The image is available at https://hub.docker.com/r/mbertani/lstm/

4. Test the image, for example by using port 9001 in you localhost:

```
$ docker run -p 9001:8888 --memory="4096m" --cpus="2" -v ./notebooks:/home/condauser/notebooks mbertani/lstm:latest
```

5. Go to `localhost:9001` to check that the jupyter server is running. Use the password `workshop` to log into it.
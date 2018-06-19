# Elasticsearch + learn-to-rank
Docker image to work with Elasticsearch and Learning to rank. 

## Setup
1. Assuming you are in the directory of the Dockerfile, run:

```
$ docker build -t mbertani/es-ltr-platinum:6.2.4 .
```

2. Push the image to dockerhub.
```
$ docker login
$ docker push mbertani/es-ltr-platinum:6.2.4
``` 

The image is available at https://hub.docker.com/r/mbertani/es-ltr-platinum/

4. Test the image, for example by using port 9001 in you localhost:

```
$ docker run -p 9200:9200 mbertani/es-ltr-platinum:6.2.4
```

5. Go to `localhost:9200` to check that elasticsearch is running with the right version.

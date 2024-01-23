# docker-images

To push a new (or updated) Dockerfile to [Docker Hub](https://hub.docker.com/repositories/yperteam):

Create a Docker image:
```sh
docker build -t <DOCKER_HUB_ID>/<REPOSITORY>:<TAG> <DOCKERFILE_PATH>
# Exemple: docker build -t yperteam/circleci-python:3.10 .
```

Check that the images is created:
```sh
docker images
```

Then, log in:
```sh
docker login
```
*credentials are in 1Password*

And, push it to Hub:
```sh
docker push <IMAGE_NAME>:<TAG>
# Exemple: docker push yperteam/circleci-python:3.10
```

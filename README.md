# docker-images

To push a new (or updated) Dockerfile to [Docker Hub](https://hub.docker.com/repositories/yperteam), run the command:
```sh
docker build -t <DOCKER_HUB_ID>/<REPOSITORY>:<TAG> <DOCKERFILE_PATH>
# Exemple: docker build -t yperteam/circleci-python:3.10 .
```

*credentials are in 1Password*
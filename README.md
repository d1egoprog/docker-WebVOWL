# Web Visual OWL - Dockerized Alternative

This repository is dedicated to expose and track a customized Docker Image of the traditional [WebVOWL](http://vowl.visualdataweb.org/webvowl.html). This build intends to be used as a dedicated service to provide for personal or small research teams.

A ready-to-use [image](https://hub.docker.com/r/d1egoprog/webvowl) from Docker Hub is provided, along with the [deploy instructions](#deploy-alternatives). The current supported version is 1.1.7.

**DISCLAIMER:** this is **not an official documentation** guide. 

## Deploy Alternatives

To deploy the prebuilt docker image, two options are provided: use the `docker compose` tool from the `docker` command from the CLI utility.

### Deploy using Docker CLI

Directly run the `docker` command like the following example.. For more information, check the [Official Documentation](http://vowl.visualdataweb.org/webvowl.html)

``` Docker
docker run -p 8080:8080 d1egoprog/webvowl:1.1.7
```

### Deploy using docker-compose

Download the prepared `compose.yaml` file from the repository via `wget` and execute the command using the utility.

``` BASH
wget https://raw.githubusercontent.com/d1egoprog/docker-WebVOWL/main/compose.yaml
docker compose -p webvowl up -d
```

The previous lines will download and run the following docker compose file.

``` YAML
version: '3.7'

services:
  server:
    image: d1egoprog/webvowl:1.1.7
    ports:
        - 8080:8080
    restart: always
```

To check the functionality, you can open a web browser window on [localhost:8080](http://localhost:8080). 

Happy hacking!! 🖖🖖.

## Contact

If you have any questions in deployment or if any error is found, please contact me or open an issue. And contributing is always welcome. The [Github repository Issues](https://github.com/d1egoprog/docker-WebVOWL/issues).
python-workspace
=====================

This repository contains **Dockerfile** for D1 team python workspace. 

More details on [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/deeone/python-workspace/) page. 

Published to the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Docker Image

* [ciandtsoftware/appengine-python-nodejs](https://registry.hub.docker.com/u/ciandtsoftware/appengine-python-nodejs/)

### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/deeone/python-workspace/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull deeone/python-workspace`

   (alternatively, you can build an image from Dockerfile: `docker build -t="deeone/python-workspace" github.com/d1-oss/docker-docker-python-workspace`)


### Usage

    docker run \
    -u 1000 \
    -it \
    -p 8083:8083 \
    --volume $SSH_AUTH_SOCK:/ssh-agent --env SSH_AUTH_SOCK=/ssh-agent \
    --volume /home/fabio/Development:/workspace \
    --hostname work \
    --name deeone \
    deeone/python-workspace
## Nginx Dockerfile


This repository contains **Dockerfile** of [Nginx](http://nginx.org/) for [Docker](https://www.docker.com/)'s [automated build]() published to the public [Docker Hub Registry](https://registry.hub.docker.com/) [![](https://badge.imagelayers.io/curratore/nginx-centos:latest.svg)](https://imagelayers.io/?images=curratore/nginx-centos:latest) [![Circle CI](https://circleci.com/gh/curratore/dockerfiles/tree/master.svg?style=svg)](https://circleci.com/gh/curratore/dockerfiles/tree/master)
## Base Docker Image

* [dockerfile/centos](https://hub.docker.com/centos/)

## Installation

1. Install [Docker](https://docs.docker.com/installation/)
2. Build an image from Dockerfile: `docker build -t nginx-centos .`

### Usage

    `docker run -d -p 80:80 dockerfiles/nginx`

#### Use persistent/shared directories

    docker run -d -p 80:80 -v <sites-enabled-dir>:/etc/nginx/sites-enabled/ -v <certs-dir>:/etc/nginx/certs -v <log-dir>:/var/log/nginx -v <html-dir>:/var/www/html dockerfile/nginx
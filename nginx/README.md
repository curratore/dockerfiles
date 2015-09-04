## Nginx Dockerfile


This repository contains **Dockerfile** of [Nginx](http://nginx.org/) for [Docker](https://www.docker.com/)'s [automated build] published to the public [Docker Hub Registry](https://registry.hub.docker.com/)

## Base Docker Image

* [dockerfile/centos]

## Installation

Build an image from Dockerfile: `docker build -t nginx-centos .` 

### Usage

    `docker run -d -p 80:80 dockerfiles/nginx`

#### Use persistent/shared directories

    docker run -d -p 80:80 -v <sites-enabled-dir>:/etc/nginx/sites-enabled/ -v <certs-dir>:/etc/nginx/certs -v <log-dir>:/var/log/nginx -v <html-dir>:/var/www/html dockerfile/nginx
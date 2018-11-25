# docker-nginx-centos

Nginx docker image based on centos official image, versions 6 and 7.

[![](https://images.microbadger.com/badges/image/chentex/docker-nginx-centos.svg)](https://microbadger.com/images/chentex/docker-nginx-centos "Get your own image badge on microbadger.com")

## What is Nginx?
Nginx (pronounced "engine x") is a web server. It can act as a reverse proxy server for HTTP, HTTPS, SMTP, POP3, and IMAP protocols, as well as a load balancer and an HTTP cache.

See: [Nginx](http://Nginx.org/)

## What is inside of this repo?
In this git repository you will find the docker image definitions for Nginx 1.14.0
in centos 7 and 6.

* `centos7/Dockerfile`
* `centos6/Dockerfile`

## How do I use this images?
To use this images you must do as follows:

```
# you can use tags latest, latest-centos7, latest-centos6
docker pull chentex/docker-nginx-centos:latest

# to run the image just execute
docker run -d -p 80:80 chentex/docker-nginx-centos:latest

# to run the with a volume for /data/www
docker run -d -p 80:80 -v /custom/volume/path:/data/www chentex/docker-nginx-centos:latest
```

You will have now a docker container running nginx on centos you can look for it with

```
docker ps
```

You can log into the container with this command

```
docker exec -ti <container-id> bash
```

## How do I build this images?
First things first, you can find these docker images in `chentex/docker-nginx-centos`
but you can also build a specific version on your own, you only need:

- docker

Clone this repo

`git clone https://github.com/chentex/docker-nginx-centos.git`

Go to the folder in your terminal and type this:

```
# cd <desired-version>
cd centos7
# Then build the new image
docker build -f Dockerfile .
```

If you want to tag your image use the following command

```
docker build -f Dockerfile -t yourbase/yourname:version .
```
---
For more on docker build reference to the [Documentation](https://docs.docker.com/engine/reference/commandline/build/)

You can get the source from the images in the [Repository](https://github.com/chentex/docker-nginx-centos)

# docker-nginx-centos

Nginx docker image based on centos official image, versions 6 and 7.

## What is Nginx?
Nginx (pronounced "engine x") is a web server. It can act as a reverse proxy server for HTTP, HTTPS, SMTP, POP3, and IMAP protocols, as well as a load balancer and an HTTP cache.

See: [Nginx](http://Nginx.org/)

## What is inside of this repo?
In this git repository you will find the docker image definitions for Nginx LTS 1.10
in centos 7 and 6.

* `centos7/Dockerfile`
* `centos6/Dockerfile`

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

For more on docker build reference to the [Documentation](https://docs.docker.com/engine/reference/commandline/build/)

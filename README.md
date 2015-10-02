docker-mysql
===========

## Description

Dockerfile for building a MySQL server.

Yes, there are [official builds](https://hub.docker.com/_/mysql/) for MySQL, but if you are running under [Docker Toolbox](https://www.docker.com/toolbox) (or [boot2docker](http://boot2docker.io/)) and mounting a host directory as a data volume, there's a [problem](https://github.com/boot2docker/boot2docker/issues/581).

This build fixes the problem by changing `uid` for `mysql` user so you'll be able to write data to a mounted host directory.

See [Docker Hub](https://hub.docker.com/r/nkwhr/mysql/tags/) for available tags.

## Usage

### Use image on Docker Hub

```
$ docker pull nkwhr/mysql:latest
$ docker run -d --name db -p 3306:3306 -v /Users/<name>/path:/var/lib/mysql nkwhr/mysql
```

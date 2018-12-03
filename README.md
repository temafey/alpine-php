# Alpine PHP 
[![Build Status](https://travis-ci.org/temafey/alpine-php.svg?branch=master)](https://travis-ci.org/temafey/alpine-php)
![Docker Pulls](https://img.shields.io/docker/pulls/temafey/alpine-php.svg?style=flat-square)



Minimal PHP Docker images based on Alpine. Contains **tags** for development environments and adapted for various frameworks like [Symfony](http://symfony.com/).


## Documentation

[Read about Documentation and see some examples here](https://github.com/temafey/alpine-php/tree/master/doc/README.md)

## Images

- [7.2](https://github.com/temafey/alpine-php/blob/master/7.2/Dockerfile)
- [7.1](https://github.com/temafey/alpine-php/blob/master/7.1/Dockerfile)
- [7.3](https://github.com/temafey/alpine-php/blob/master/7.3/Dockerfile)

## Dev Dockerfiles

Dev images extend the standard ones and add some tools for development and CI like, composer, xdebug, etc...

| General purpose     | Symfony
|---------------------|--------------
| [7.2-dev](https://github.com/temafey/alpine-php/blob/master/7.2/Dockerfile.dev), [7.2-front](https://github.com/temafey/alpine-php/blob/master/7.2/Dockerfile.front) | [7.2-dev-sf](https://github.com/temafey/alpine-php/blob/symfony/7.2/Dockerfile.dev), [7.2-front-sf](https://github.com/temafey/alpine-php/blob/symfony/7.2/Dockerfile.front)
| [7.1-dev](https://github.com/temafey/alpine-php/blob/master/7.1/Dockerfile.dev), [7.1-front](https://github.com/temafey/alpine-php/blob/master/7.1/Dockerfile.front) | [7.1-dev-sf](https://github.com/temafey/alpine-php/blob/symfony/7.1/Dockerfile.dev), [7.1-front-sf](https://github.com/temafey/alpine-php/blob/symfony/7.1/Dockerfile.front)
| [7.3-dev](https://github.com/temafey/alpine-php/blob/master/7.3/Dockerfile.dev) | [7.3-dev-sf](https://github.com/temafey/alpine-php/blob/symfony/7.3/Dockerfile.dev)

## Usage:

```sh
docker run -d --name dev -p 9000:9000 -p 2323:22 -v $PWD:/app temafey/alpine-php:7.2-dev
```

> SSH is only for IDE integration to use container as remote interpreter 

## Content table

|    Tag     | Parent     |        Content
|------------|------------|-----------------------------------------------------------------------------------
| 7.1        |   alpine   | tini, php7.1-cli & fpm
| 7.1-dev    |    7.1     | + SSH server, xdebug, ant, composer
| 7-dev-sf   |   7.1-dev  | + [Symfony aliases](https://github.com/temafey/alpine-php/blob/symfony/README.md)
| 7.1-front  |  7.1-dev   | + node6 & npm3 & yarn
| 7.2        |   alpine   | tini, php7.2-cli & fpm
| 7.2-dev    |    7.2     | + SSH server, xdebug, composer
| 7.2-dev-sf |   7.2-dev  | + [Symfony aliases](https://github.com/temafey/alpine-php/blob/symfony/README.md)
| 7.2-front  |  7.2-dev   | + node6 & npm3 & yarn
| 7.3        |   alpine   | tini, php7.3-cli & fpm
| 7.3-dev    |    7.3     | + SSH server, xdebug, ant, composer
| 7.3-dev-sf |   7.3-dev  | + [Symfony aliases](https://github.com/temafey/alpine-php/blob/symfony/README.md)


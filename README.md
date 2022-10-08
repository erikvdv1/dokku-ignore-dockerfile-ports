# dokku-ignore-dockerfile-ports

Dokku plugin to ignore exposed ports in Dockerfiles. When enabled an app must respect the `PORT` environment variable.

## Requirements

- dokku 0.4.0+

## Installation

```shell
# on 0.4.x
dokku plugin:install https://github.com/erikvdv1/dokku-ignore-dockerfile-ports.git ignore-dockerfile-ports
```

## Hooks

This plugin provides hooks:

* `pre-release-dockerfile`: Unsets the `DOKKU_DOCKERFILE_PORTS` config variable.

## Usage

This plugin allows you to ignore the exposed ports defined in a Dockerfile and defaults to the `PORT` environment variable. Set `DOKKU_IGNORE_DOCKERFILE_PORTS=1` to enable this plugin.

```
$ dokku config:set <app> DOKKU_IGNORE_DOCKERFILE_PORTS=1
```
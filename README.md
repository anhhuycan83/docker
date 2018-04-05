# p6-docker

> All docker image for PicoSix

## Nginx Proxy

```shell
$ docker build --force-rm -t picosix/nginx-proxy $(pwd)/nginx-proxy
```

## Nginx

```shell
$ docker build --force-rm -t picosix/nginx $(pwd)/nginx
```

## Node

```shell
$ docker build --force-rm -t picosix/node $(pwd)/node
```

## Node Puppeteer

```shell
$ docker build --force-rm -t picosix/node-puppeteer $(pwd)/node-puppeteer
```

## Node Alpine

```shell
$ docker build --force-rm -t picosix/node-alpine $(pwd)/node-alpine
```

## Mariadb

```shell
$ docker build --force-rm -t picosix/mariadb $(pwd)/mariadb
```

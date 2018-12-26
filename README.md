# p6-docker

> All docker image for PicoSix

## Mariadb

```shell
docker build --force-rm -t picosix/mariadb $(pwd)/mariadb
```

## Nginx

```shell
docker build --force-rm -t picosix/nginx $(pwd)/nginx/1
```

## Nginx Proxy

```shell
docker build --force-rm -t picosix/nginx-proxy $(pwd)/nginx/proxy
```

## Node

```shell
docker build --force-rm -t picosix/node:8 $(pwd)/node/8
```

## Node Puppeteer

```shell
docker build --force-rm -t picosix/node:puppeteer $(pwd)/node/puppeteer
```

# p6-docker

> All docker image for PicoSix

## ELK

### Start Elasticsearch and Kibana

Copy `elk/.env.example` to `elk/.env`

If you haven't been started Elasticsearch and Kibana yet, start it by command

```shell
docker-compose up -d
```

### Start Logstash

#### Build image

If you haven't been built Logstash yet, build it by command. You **MUST** find approriate environment variables from `.env` and pass it to build command

```shell
docker build -t elk_logstash --build-arg ELK_VERSION=6.5.4 .
```

#### Start Logstash container

If your project is located on same server with your logging service (Elasticsearch and Kibana).

```shell
docker run -d --name elk_logstash_1 \
-v __LOGSTASH_CONFIG__/logstash.yml:/usr/share/logstash/config/logstash.yml \
-v __LOGSTASH_PIPLINE__:/usr/share/logstash/pipeline \
-v __LOGS_FOLDER__:/logs \
-p 5044:5044 \
-e LS_JAVA_OPTS="-Xmx256m -Xms256m" \
--network elk_elk \
--link elk_elasticsearch_1:elasticsearch \
elk_logstash
```

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

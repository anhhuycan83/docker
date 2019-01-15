FROM nginx:1

RUN mkdir /app
WORKDIR /app

COPY ./nginx-proxy.conf /etc/nginx/conf.d/nginx-proxy.conf

EXPOSE 80
EXPOSE 443
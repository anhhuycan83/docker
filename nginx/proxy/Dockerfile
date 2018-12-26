FROM jwilder/nginx-proxy

# Set timezone to Ho Chi Minh City
ENV TZ=Asia/Ho_Chi_Minh
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

COPY ./nginx-proxy.conf /etc/nginx/conf.d/nginx-proxy.conf
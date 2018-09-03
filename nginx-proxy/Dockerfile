FROM jwilder/nginx-proxy

# Set timezone to Ho Chi Minh City
ENV TZ=Asia/Ho_Chi_Minh
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN { \
  echo 'client_body_buffer_size 128m;'; \
  echo 'client_max_body_size 128m;'; \
  } > /etc/nginx/conf.d/nginx-proxy.conf
FROM nginx:1

RUN mkdir /app
WORKDIR /app

# Set timezone to Ho Chi Minh City
ENV TZ=Asia/Ho_Chi_Minh
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

EXPOSE 80
EXPOSE 443
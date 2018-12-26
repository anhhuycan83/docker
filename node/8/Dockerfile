FROM node:8

RUN mkdir /app
WORKDIR /app

# Fix timezone to Ho Chi Minh City
ENV TZ=Asia/Ho_Chi_Minh
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

EXPOSE 9001
EXPOSE 9002
EXPOSE 9003
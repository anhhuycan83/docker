FROM mariadb:10

# Set timezone to Ho Chi Minh City
ENV TZ=Asia/Ho_Chi_Minh
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

CMD ["--character-set-server=utf8", "--collation-server=utf8_unicode_ci"]
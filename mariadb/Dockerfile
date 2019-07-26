FROM mariadb:latest

RUN apt-get update
RUN apt-get install language-pack-ja -y
RUN update-locale LANG=ja_JP.UTF-8

COPY ./my.cnf /etc/mysql/conf.d/my.cnf

CMD ["mysqld"]

EXPOSE 3306

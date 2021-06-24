# docker build --rm=true -t custom-mysql .
# docker run -m 300M --name mysql -p 3306:3306 -v D:/mysql-data-dir:/var/lib/mysql -d custom-mysql
# docker exec -it mysql bash
# docker update --restart=always mysql

FROM mysql:5.7.31

MAINTAINER XueWu

ADD cnf/mysqld.cnf /etc/mysql/mysql.conf.d

ENV MYSQL_ROOT_PASSWORD=root2020@ABC

EXPOSE 3306

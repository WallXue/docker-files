# docker build --rm=true -t custom-elasticsearch:1.0-es-6.3.2 .
# docker run --name elasticsearch -it -p 9200:9200 -d custom-elasticsearch:1.0-es-6.3.2
# docker exec -it elasticsearch bash
#				-u 0   root
# docker update --restart=always elasticsearch
# 复制文件到容器中 docker cp source/elasticsearch-6.3.2.zip elasticsearch:/usr/local/lib/es-6.3.2/
FROM centos:centos7

MAINTAINER XueWu

RUN yum install java-1.8.0-openjdk -y
RUN useradd es

ADD --chown=es package/elasticsearch-6.3.2.tar.gz /home/es
COPY --chown=es cnf/* /home/es/elasticsearch-6.3.2/conf/
RUN chown -R es /home/es/elasticsearch-6.3.2

USER es
WORKDIR /home/es/elasticsearch-6.3.2
EXPOSE 9200

#CMD ["sh", "/home/es/elasticsearch-6.3.2/bin/elasticsearch"]
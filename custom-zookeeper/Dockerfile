# docker build --rm=true -t custom-zookeeper .
# docker run --name zookeeper -p 2181:2181 -d custom-zookeeper
# docker exec -it zookeeper sh
# docker update --restart=always zookeeper

FROM zookeeper:3.6.2

MAINTAINER XueWu

ADD cnf/zoo.cfg /apache-zookeeper-3.6.2-bin/conf/zoo.cfg
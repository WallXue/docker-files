# docker build --rm=true -t custom-redis .
# docker run -m 100m --name redis -p 6379:6379 -d custom-redis
# docker exec -it redis sh
# docker update --restart=always redis

FROM redis:4.0.14

MAINTAINER XueWu

ADD cnf/redis.conf /usr/local/etc/redis/redis.conf

CMD [ "redis-server", "/usr/local/etc/redis/redis.conf" ]

EXPOSE 6379

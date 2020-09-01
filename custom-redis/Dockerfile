# docker build --rm=true -t custom-redis .
# docker run --name redis -p 6379:6379 -d custom-redis
# docker exec -it redis sh
# docker update --restart=always redis

FROM redis:4.0.14

MAINTAINER XueWu <xuewu@xcxd.com>

ADD cnf/redis.conf /usr/local/etc/redis/redis.conf

CMD [ "redis-server", "/usr/local/etc/redis/redis.conf" ]

EXPOSE 6379
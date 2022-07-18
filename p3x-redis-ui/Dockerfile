FROM node:18-alpine

ARG version
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.tuna.tsinghua.edu.cn/g' /etc/apk/repositories

ENV COMPOSER_PROCESS_TIMEOUT=3600
ENV DEBIAN_FRONTEND=noninteractive
ENV P3XRS_DOCKER_HOME=/settings
EXPOSE 7843

RUN npm -g --unsafe-perm install p3x-redis-ui@${version} --registry=https://registry.npmmirror.com
CMD p3x-redis

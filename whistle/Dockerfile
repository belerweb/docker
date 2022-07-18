FROM node:18-alpine

ARG version
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.tuna.tsinghua.edu.cn/g' /etc/apk/repositories
RUN npm install -g whistle@${version} --registry=https://registry.npmmirror.com

EXPOSE 8899
ENTRYPOINT ["w2"]



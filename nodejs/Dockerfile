FROM node:10.15.3-alpine

RUN apk --update add git less openssh && \
    rm -rf /var/lib/apt/lists/* && \
    rm /var/cache/apk/* && cd /home/node &&\
    git clone https://github.com/arcmop/retobase-nodejs.git && \
    cd /home/node/retobase-nodejs && npm install -g express --save
WORKDIR /home/node/retobase-nodejs
EXPOSE 4000
CMD ["node", "server.js"]

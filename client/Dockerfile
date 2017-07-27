FROM node:8.2.1

RUN apt-get update \
  && apt-get install -y \
    git \
  && rm -rf /var/lib/apt/lists/*

WORKDIR /opt

RUN git clone https://github.com/JordyMoos/elm-yapm-client.git

WORKDIR /opt/elm-yapm-client

RUN npm install && npm install -g http-server

ADD ./config.json /opt/elm-yapm-client/config.json

RUN npm run prod \
  && rm dist/remove-me.js

EXPOSE 80

CMD ["http-server", "/opt/elm-yapm-client/dist", "-p 80"]


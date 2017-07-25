FROM node:8.2.1

RUN apt-get update \
  && apt-get install -y \
    git \
  && rm -rf /var/lib/apt/lists/*

WORKDIR /opt

RUN git clone https://github.com/JordyMoos/elm-yapm-client.git

WORKDIR /opt/elm-yapm-client

RUN npm install

ADD ./config.json /opt/elm-yapm-client/config.json

RUN npm run prod \
  && rm dist/remove-me.js

CMD ["echo", "Elm client build"]


FROM alpine:3.3
MAINTAINER Ilkka Laukkanen <ilkka@ilkka.io>

RUN apk --no-cache add --virtual build-deps curl

RUN mkdir -p /caddy /caddy/log \
  && curl -L "https://caddyserver.com/download/build?os=linux&arch=386&features=" | tar xzf - -C /caddy

RUN apk del build-deps

WORKDIR /caddy
COPY Caddyfile /caddy/

EXPOSE 2015

CMD ["./caddy"]

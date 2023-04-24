ARG TRAEFIK_VERSION=v2.9
FROM traefik:${TRAEFIK_VERSION}

LABEL maintainer="Truong Thanh Tung <ttungbmt@gmail.com>"

RUN apk add curl busybox-extras vim

RUN mkdir -p /etc/traefik/acme \
  && touch /etc/traefik/acme/acme.json \
  && chmod 600 /etc/traefik/acme/acme.json
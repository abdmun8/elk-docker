FROM alpine:3.8

WORKDIR /usr/share/curator
ENV CURATOR_VERSION=5.8

RUN apk --update add --no-cache tini python py-pip
RUN pip --disable-pip-version-check install elasticsearch-curator==${CURATOR_VERSION}

COPY entrypoint.sh /
COPY config ./config

ENTRYPOINT ["/entrypoint.sh"]


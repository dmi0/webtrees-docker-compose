FROM alpine

ARG WEBTREES_VERSION

WORKDIR /var/www/html

RUN apk update && apk add wget \
    && wget https://github.com/fisharebest/webtrees/archive/$WEBTREES_VERSION.tar.gz \
    && tar -xzf $WEBTREES_VERSION.tar.gz --strip-components=1 \
    && chown -R 1000 /var/www/html \
    && chmod -R g-w /var/www/html*
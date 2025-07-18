FROM        --platform=$TARGETOS/$TARGETARCH node:22-alpine

LABEL       author="Torsten Widmann" maintainer="info@goover.de"
LABEL       org.opencontainers.image.source="https://github.com/gOOvER/own-pterodactyl-images"
LABEL       org.opencontainers.image.licenses=MIT

RUN         apk update \
            && apk upgrade

RUN         apk add --no-cache \
                autoconf \
                automake \
                build-base \
                ca-certificates\
                chromium \
                curl \
                bind-tools \
				ffmpeg \
                g++ \
                git \
                gpg \
                gnupg \
                iproute2 \
                iputils-ping \
                libtool \
                musl \
                musl-utils \
                musl-locales \
                python3 \
                python3-dev \
                py3-pip \
                pipx \
                sqlite \
                tzdata \
                zip \
                libc6-compat \
                tini

# updating npm 
RUN         npm install npm@latest -g

# download cloudflared
ARG         TARGETPLATFORM
RUN         if [ "$TARGETPLATFORM" = "linux/amd64" ]; then ARCHITECTURE=amd64; elif [ "$TARGETPLATFORM" = "linux/arm64" ]; then ARCHITECTURE=arm64; fi \
            && curl -L https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-${ARCHITECTURE} -o /usr/bin/cloudflared
RUN         chmod +x /usr/bin/cloudflared

# install apprise
RUN         pipx install apprise

## Setup user and working directory
RUN         adduser -D -h /home/container container -s /bin/bash container
USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

STOPSIGNAL SIGINT

COPY        --chown=container:container ./entrypoint.sh /entrypoint.sh
RUN         chmod +x /entrypoint.sh
ENTRYPOINT    ["/sbin/tini", "-g", "--"]
CMD         ["/entrypoint.sh"]
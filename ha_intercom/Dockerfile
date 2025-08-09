ARG BUILD_FROM=ghcr.io/hassio-addons/base:15.0.7
FROM ${BUILD_FROM}

RUN apk add --no-cache ffmpeg nodejs npm git

WORKDIR /opt
RUN git clone --depth=1 https://github.com/JoeHogan/ha-intercom.git app
WORKDIR /opt/app
RUN npm ci --omit=dev

COPY rootfs /

EXPOSE 3001

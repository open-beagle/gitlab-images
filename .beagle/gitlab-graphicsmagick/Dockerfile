ARG BUILD_IMAGE=registry.cn-qingdao.aliyuncs.com/wod/debian:buster-slim
ARG BASE_IMAGE=registry.cn-qingdao.aliyuncs.com/wod/alpine:3.13

FROM ${BUILD_IMAGE} as compile

ARG GM_VERSION_MINOR=1.3
ARG GM_VERSION=1.3.36
ARG _SIGNATURE_KEY=EBDFDB21B020EE8FD151A88DE301047DE1198975
ARG _SIGNATURE_ENFORCE=1

ENV GM_SOURCE_URL="https://ftp.icm.edu.pl/pub/unix/graphics/GraphicsMagick/${GM_VERSION_MINOR}/GraphicsMagick-${GM_VERSION}.tar.xz"
ENV GM_SIGNATURE_URL="${SOURCE_URL}.sig"

RUN mkdir -p /build /target
COPY scripts/ /scripts

RUN /scripts/dependencies
RUN /scripts/download
RUN /scripts/build

FROM ${BASE_IMAGE}
COPY --from=compile /target/ /

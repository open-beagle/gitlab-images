ARG GITLAB_GO_IMAGE="registry.gitlab.com/gitlab-org/build/cng/gitlab-go:master"
ARG BASE=registry.cn-qingdao.aliyuncs.com/wod/alpine:3.13

FROM ${GITLAB_GO_IMAGE} as compile

ARG GITLAB_LOGGER_VERSION=v1.1.0
ARG GITLAB_LOGGER_SHA256=2a5a97bc93feecfe4eec69131091172fe291989dfb00a1b39f890ffcc51c1e52

ENV GITLAB_LOGGER_SOURCE_URL="https://gitlab.com/gitlab-org/charts/components/gitlab-logger/-/archive/${GITLAB_LOGGER_VERSION}/gitlab-logger-${GITLAB_LOGGER_VERSION}.tar.gz"

RUN mkdir -p /build /target
COPY scripts/ /scripts

RUN /scripts/dependencies
RUN /scripts/download
RUN /scripts/build

FROM ${BASE}
COPY --from=compile /target/ /

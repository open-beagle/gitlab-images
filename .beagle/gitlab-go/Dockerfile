ARG FROM_IMAGE="$CI_REGISTRY_IMAGE/gitlab-ruby"

FROM ${FROM_IMAGE}

ARG GO_VERSION=1.16.4
ARG GO_ARCH=amd64
ARG BUILD_DIR=/tmp/build

ENV GO_URL="https://storage.googleapis.com/golang/go${GO_VERSION}.linux-${GO_ARCH}.tar.gz"
ENV GOPATH="/go"

# install go
RUN mkdir ${BUILD_DIR} \
  && cd ${BUILD_DIR} \
  && curl --retry 6 -so golang.tar.xz ${GO_URL} \
  && tar -xf golang.tar.xz \
  && mv ${BUILD_DIR}/go /usr/local/go \
  && rm golang.tar.xz \
  && rm -rf /var/lib/apt/lists/* \
  && ln -sf /usr/local/go/bin/go /usr/local/go/bin/gofmt /usr/local/go/bin/godoc /usr/local/bin/ \
  && rm -rf ${BUILD_DIR}

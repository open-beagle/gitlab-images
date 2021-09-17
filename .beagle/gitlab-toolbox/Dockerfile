ARG PYTHON_IMAGE="registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-python:3.8.9-amd64"
ARG RAILS_IMAGE="registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-rails:v14.2.3-amd64"
ARG GITALY_IMAGE="registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-logger:v1.1.0-amd64"
ARG PYTHON_IMAGE="registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-python:3.8.9-amd64"

FROM ${PYTHON_IMAGE} AS python

FROM ${GITALY_IMAGE} AS gitaly

FROM ${RAILS_IMAGE}

ARG S3CMD_VERSION="2.1.0"
ARG GSUTIL_VERSION="4.43"

COPY --from=python /usr/local/bin /usr/local/bin/
COPY --from=python /usr/local/lib /usr/local/lib/
COPY --from=python /usr/local/include /usr/local/include/
COPY --from=gitaly  /usr/local/bin/gitaly-backup /usr/local/bin/

RUN apt-get update \
	&& apt-get install -y --no-install-recommends \
  gcc \
  ca-certificates \
  openssl \
  tar \
  && ldconfig \
  && pip3 install --upgrade s3cmd==${S3CMD_VERSION} \
  && pip3 install gsutil==${GSUTIL_VERSION} crcmod \
  && apt-get purge -y --auto-remove gcc \
  && rm -rf /var/lib/apt/lists/*

ARG GITLAB_USER=git

COPY scripts/bin/* /usr/local/bin/
COPY scripts/lib/* /usr/lib/ruby/vendor_ruby/

USER $GITLAB_USER:$GITLAB_USER

ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]

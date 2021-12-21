ARG RAILS_IMAGE="registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-rails:v14.2.3"
ARG GITALY_IMAGE="registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-gitaly:v14.2.3"
ARG PYTHON_IMAGE="registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-python:3.8.9"

FROM ${PYTHON_IMAGE} AS python

FROM ${GITALY_IMAGE} AS gitaly

FROM ${RAILS_IMAGE}

ARG S3CMD_VERSION="2.1.0"
ARG GSUTIL_VERSION="4.43"

COPY --from=python /usr/local/bin /usr/local/bin/
COPY --from=python /usr/local/lib /usr/local/lib/
COPY --from=python /usr/local/include /usr/local/include/
COPY --from=gitaly  /usr/local/bin/gitaly-backup /usr/local/bin/
COPY --from=gitaly /usr/bin/git /usr/bin/git-cvsserver /usr/bin/git-shell /usr/bin/
RUN ln -s /usr/bin/git /usr/bin/git-receive-pack && \
ln -s /usr/bin/git /usr/bin/git-upload-archive && \
ln -s /usr/bin/git /usr/bin/git-upload-pack

RUN apt-get update \
	&& apt-get install -y --no-install-recommends \
  gcc \
  ca-certificates \
  openssl \
  tar \
  && ldconfig \
  && curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | bash -s -- -y \
  && . $HOME/.cargo/env \
  && pip3 install --upgrade s3cmd==${S3CMD_VERSION} \
  && pip3 install gsutil==${GSUTIL_VERSION} crcmod \
  && apt-get purge -y --auto-remove gcc \
  && rm -rf /var/lib/apt/lists/*

ARG GITLAB_USER=git

COPY scripts/bin/* /usr/local/bin/
COPY scripts/lib/* /usr/lib/ruby/vendor_ruby/

USER $GITLAB_USER:$GITLAB_USER

ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]

ARG BASE="registry.cn-qingdao.aliyuncs.com/wod/debian:bullseye-slim"
FROM ${BASE}

ARG BUILD_DIR=/tmp/build
ARG PYTHON_VERSION="3.8.9"

RUN buildDeps=' \
  build-essential \
  ca-certificates \
  curl \
  file \
  gcc \
  libffi-dev \
  libssl-dev \
  make \
  zlib1g-dev' && \
  apt-get update && \
  apt-get install -y --no-install-recommends $buildDeps && \
  mkdir ${BUILD_DIR} && \
  curl --retry 6 -fsSL https://www.python.org/ftp/python/${PYTHON_VERSION}/Python-${PYTHON_VERSION}.tgz \
  | tar -xz -C ${BUILD_DIR}  && \
  cd ${BUILD_DIR}/Python-${PYTHON_VERSION} && \
  ./configure --enable-shared --with-readline=editline --with-dbmliborder= && make && \
  make install && \
  ldconfig && \
  pip3 install --upgrade pip setuptools && \
  rm -rf /usr/local/lib/python.3.8/lib-dynload/dbm.* && \
  rm -rf /usr/local/lib/python.3.8/lib-dynload/_sqlite3.* && \
  rm -rf /usr/local/lib/python.3.8/test && \
  find /usr/local/lib/python3.8 -name '__pycache__' -type d -print -exec rm -r {} + && \
  apt-get purge -y $buildDeps && \
  rm -rf /var/lib/apt/list/* && \
  rm -rf ${BUILD_DIR}

CMD [ "python" ]

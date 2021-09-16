# gitlab-python

```bash
# amd64
docker build \
  --build-arg PYTHON_VERSION=3.8.9 \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/debian:bullseye-slim-amd64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-python:3.8.9-amd64 \
  --file ./.beagle/gitlab-python/Dockerfile ./.beagle/gitlab-python/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-python:3.8.9-amd64

# arm64
docker build \
  --build-arg python_MINOR_VERSION=3.8.9 \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/debian:bullseye-slim-arm64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-python:3.8.9-arm64 \
  --file ./.beagle/gitlab-python/Dockerfile ./.beagle/gitlab-python/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-python:3.8.9-arm64

# ppc64le
docker build \
  --build-arg python_MINOR_VERSION=3.8.9 \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/debian:bullseye-slim-ppc64le \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-python:3.8.9-ppc64le \
  --file ./.beagle/gitlab-python/Dockerfile ./.beagle/gitlab-python/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-python:3.8.9-ppc64le
```

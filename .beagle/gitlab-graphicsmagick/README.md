# gitlab-graphicsmagick

```bash
# amd64
docker build \
  --build-arg BUILD_IMAGE=registry.cn-qingdao.aliyuncs.com/wod/debian:buster-slim-amd64 \
  --build-arg BASE_IMAGE=registry.cn-qingdao.aliyuncs.com/wod/alpine:3.13-amd64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-graphicsmagick:1.3.36-amd64 \
  --file ./.beagle/gitlab-graphicsmagick/Dockerfile ./.beagle/gitlab-graphicsmagick/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-graphicsmagick:1.3.36-amd64

# arm64
docker build \
  --build-arg BUILD_IMAGE=registry.cn-qingdao.aliyuncs.com/wod/debian:buster-slim-arm64 \
  --build-arg BASE_IMAGE=registry.cn-qingdao.aliyuncs.com/wod/alpine:3.13-arm64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-graphicsmagick:1.3.36-arm64 \
  --file ./.beagle/gitlab-graphicsmagick/Dockerfile ./.beagle/gitlab-graphicsmagick/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-graphicsmagick:1.3.36-arm64

# ppc64le
docker build \
  --build-arg BUILD_IMAGE=registry.cn-qingdao.aliyuncs.com/wod/debian:buster-slim-ppc64le \
  --build-arg BASE_IMAGE=registry.cn-qingdao.aliyuncs.com/wod/alpine:3.13-ppc64le \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-graphicsmagick:1.3.36-ppc64le \
  --file ./.beagle/gitlab-graphicsmagick/Dockerfile ./.beagle/gitlab-graphicsmagick/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-graphicsmagick:1.3.36-ppc64le
```

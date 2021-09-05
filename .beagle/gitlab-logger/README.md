# gitlab-logger

```bash
# amd64
docker build \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/alpine:3.13-amd64 \
  --build-arg GITLAB_GO_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-go:v1.16.7-amd64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-logger:v1.1.0-amd64 \
  --file ./.beagle/gitlab-logger/Dockerfile ./.beagle/gitlab-logger/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-logger:v1.1.0-amd64

# arm64
docker build \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/alpine:3.13-arm64 \
  --build-arg GITLAB_GO_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-go:v1.16.7-arm64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-logger:v1.1.0-arm64 \
  --file ./.beagle/gitlab-logger/Dockerfile ./.beagle/gitlab-logger/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-logger:v1.1.0-arm64

# ppc64le
docker build \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/alpine:3.13-ppc64le \
  --build-arg GITLAB_GO_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-go:v1.16.7-ppc64le \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-logger:v1.1.0-ppc64le \
  --file ./.beagle/gitlab-logger/Dockerfile ./.beagle/gitlab-logger/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-logger:v1.1.0-ppc64le
```

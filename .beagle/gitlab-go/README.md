# gitlab-go

```bash
# amd64
docker build \
  --build-arg CI_REGISTRY_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm \
  --build-arg TAG=2.7.2-amd64 \
  --build-arg GO_VERSION=1.16.7 \
  --build-arg GO_ARCH=amd64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-go:v1.16.7-amd64 \
  --file ./.beagle/gitlab-go/Dockerfile ./.beagle/gitlab-go/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-go:v1.16.7-amd64

# arm64
docker build \
  --build-arg CI_REGISTRY_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm \
  --build-arg TAG=2.7.2-arm64 \
  --build-arg GO_VERSION=1.16.7 \
  --build-arg GO_ARCH=arm64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-go:v1.16.7-arm64 \
  --file ./.beagle/gitlab-go/Dockerfile ./.beagle/gitlab-go/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-go:v1.16.7-arm64

# ppc64le
docker build \
  --build-arg CI_REGISTRY_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm \
  --build-arg TAG=2.7.2-ppc64le \
  --build-arg GO_VERSION=1.16.7 \
  --build-arg GO_ARCH=ppc64le \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-go:v1.16.7-ppc64le \
  --file ./.beagle/gitlab-go/Dockerfile ./.beagle/gitlab-go/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-go:v1.16.7-ppc64le
```

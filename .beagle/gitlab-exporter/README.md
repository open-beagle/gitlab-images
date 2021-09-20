# gitlab-exporter

```bash
# amd64
docker build \
  --build-arg FROM_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.4-amd64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod/gitlab-exporter:11.2.0-amd64 \
  --file ./.beagle/gitlab-exporter/Dockerfile ./.beagle/gitlab-exporter/

docker push registry.cn-qingdao.aliyuncs.com/wod/gitlab-exporter:11.2.0-amd64

# arm64
docker build \
  --build-arg FROM_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.4-arm64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod/gitlab-exporter:11.2.0-arm64 \
  --file ./.beagle/gitlab-exporter/Dockerfile ./.beagle/gitlab-exporter/

docker push registry.cn-qingdao.aliyuncs.com/wod/gitlab-exporter:11.2.0-arm64


# ppc64le
docker build \
  --build-arg FROM_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.4-ppc64le \
  --tag registry.cn-qingdao.aliyuncs.com/wod/gitlab-exporter:11.2.0-ppc64le \
  --file ./.beagle/gitlab-exporter/Dockerfile ./.beagle/gitlab-exporter/

docker push registry.cn-qingdao.aliyuncs.com/wod/gitlab-exporter:11.2.0-ppc64le
```

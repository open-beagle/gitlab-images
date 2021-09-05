# gitlab-ruby

```bash
# amd64
docker build \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/debian:buster-slim-amd64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.2-amd64 \
  --file ./.beagle/gitlab-ruby/Dockerfile ./.beagle/gitlab-ruby/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.2-amd64

# arm64
docker build \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/debian:buster-slim-arm64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.2-arm64 \
  --file ./.beagle/gitlab-ruby/Dockerfile ./.beagle/gitlab-ruby/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.2-arm64

# ppc64le
docker build \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/debian:buster-slim-ppc64le \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.2-ppc64le \
  --file ./.beagle/gitlab-ruby/Dockerfile ./.beagle/gitlab-ruby/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.2-ppc64le
```

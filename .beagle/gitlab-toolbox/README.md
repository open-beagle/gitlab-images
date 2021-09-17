# gitlab-ruby

```bash
# amd64
docker build \
  --build-arg RUBY_MINOR_VERSION=2.7.4 \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/debian:bullseye-slim-amd64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.4-amd64 \
  --file ./.beagle/gitlab-ruby/Dockerfile ./.beagle/gitlab-ruby/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.4-amd64

# arm64
docker build \
  --build-arg RUBY_MINOR_VERSION=2.7.4 \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/debian:bullseye-slim-arm64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.4-arm64 \
  --file ./.beagle/gitlab-ruby/Dockerfile ./.beagle/gitlab-ruby/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.4-arm64


# ppc64le
docker build \
  --build-arg RUBY_MINOR_VERSION=2.7.4 \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/debian:bullseye-slim-ppc64le \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.4-ppc64le \
  --file ./.beagle/gitlab-ruby/Dockerfile ./.beagle/gitlab-ruby/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-ruby:2.7.4-ppc64le
```

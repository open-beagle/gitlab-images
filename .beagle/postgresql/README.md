# gitlab-postgresql

```bash
# amd64
docker build \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/debian:bullseye-slim-amd64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-postgresql:13.2-amd64 \
  --file ./.beagle/postgresql/Dockerfile ./.beagle/postgresql/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-postgresql:13.2-amd64

# arm64
docker build \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/debian:bullseye-slim-arm64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-postgresql:13.2-arm64 \
  --file ./.beagle/postgresql/Dockerfile ./.beagle/postgresql/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-postgresql:13.2-arm64

# ppc64le
docker build \
  --build-arg BASE=registry.cn-qingdao.aliyuncs.com/wod/debian:bullseye-slim-ppc64le \
  --tag registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-postgresql:13.2-ppc64le \
  --file ./.beagle/postgresql/Dockerfile ./.beagle/postgresql/

docker push registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-postgresql:13.2-ppc64le
```

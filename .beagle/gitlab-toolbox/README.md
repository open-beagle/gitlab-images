# gitlab-toolbox

```bash
# amd64
docker build \
  --build-arg RAILS_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-rails:v14.2.3-amd64 \
  --build-arg GITALY_IMAGE=registry.cn-qingdao.aliyuncs.com/wod/gitlab-gitaly:v14.2.3-amd64 \
  --build-arg PYTHON_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-python:3.8.9-amd64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod/gitlab-toolbox:v14.2.3-amd64 \
  --file ./.beagle/gitlab-toolbox/Dockerfile ./.beagle/gitlab-toolbox/

docker push registry.cn-qingdao.aliyuncs.com/wod/gitlab-toolbox:v14.2.3-amd64

# arm64
docker build \
  --build-arg RAILS_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-rails:v14.2.3-arm64 \
  --build-arg GITALY_IMAGE=registry.cn-qingdao.aliyuncs.com/wod/gitlab-gitaly:v14.2.3-arm64 \
  --build-arg PYTHON_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-python:3.8.9-arm64 \
  --tag registry.cn-qingdao.aliyuncs.com/wod/gitlab-toolbox:v14.2.3-arm64 \
  --file ./.beagle/gitlab-toolbox/Dockerfile ./.beagle/gitlab-toolbox/

docker push registry.cn-qingdao.aliyuncs.com/wod/gitlab-toolbox:v14.2.3-arm64


# ppc64le
docker build \
  --build-arg RAILS_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-rails:v14.2.3-ppc64le \
  --build-arg GITALY_IMAGE=registry.cn-qingdao.aliyuncs.com/wod/gitlab-gitaly:v14.2.3-ppc64le \
  --build-arg PYTHON_IMAGE=registry.cn-qingdao.aliyuncs.com/wod-arm/gitlab-python:3.8.9-ppc64le \
  --tag registry.cn-qingdao.aliyuncs.com/wod/gitlab-toolbox:v14.2.3-ppc64le \
  --file ./.beagle/gitlab-toolbox/Dockerfile ./.beagle/gitlab-toolbox/

docker push registry.cn-qingdao.aliyuncs.com/wod/gitlab-toolbox:v14.2.3-ppc64le
```

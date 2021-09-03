# GitLab

```bash
git remote add upstream git@gitlab.com:gitlab-org/build/CNG.git

git fetch upstream

git merge v14.2.3
```

## charts

```bash
helm repo add gitlab https://charts.gitlab.io/
helm repo update
helm pull gitlab/gitlab
```

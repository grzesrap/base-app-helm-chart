# base-app-helm-chart

https://medium.com/@mattiaperi/create-a-public-helm-chart-repository-with-github-pages-49b180dbb417

```
helm create helm-chart-sources/base-app 
helm lint helm-chart-sources/*
helm template test -n test ./helm-chart-sources/*

helm package helm-chart-sources/*
helm repo index --url https://grzesrap.github.io/base-app-helm-chart/ .
```
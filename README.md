# base-app-helm-chart

https://medium.com/@mattiaperi/create-a-public-helm-chart-repository-with-github-pages-49b180dbb417

## How to create charts

```
helm create helm-chart-sources/base-app 
helm lint helm-chart-sources/*
helm template test -n test ./helm-chart-sources/*
```
## How to add version
```
helm package helm-chart-sources/*
helm repo index --url https://grzesrap.github.io/base-app-helm-chart/ .
helm repo index --url https://grzesrap.github.io/base-app-helm-chart/ --merge index.yaml .
```
## How to use
```
helm repo add grzesrap https://grzesrap.github.io/base-app-helm-chart/
helm repo update
helm search repo base-app -l
```

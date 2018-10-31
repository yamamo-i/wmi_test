# docker-composeでの構築

## prometheus

### 前提条件

* local上のWindowsでwmi_exporterを起動していること

### local_promのbuild

```sh
$ (cd prometheus_local&&docker build -t local_prom .)
```

### Grafana

* 何かあれば記述

## prometheusの起動

```sh
$ docker-compose -f monitoring.yml up -d
```

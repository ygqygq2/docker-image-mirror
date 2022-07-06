# 镜像仓库转换

Uses/如何拉取新镜像
-------
[创建issues](https://github.com/ygqygq2/docker-image-mirror/issues/new?assignees=&labels=porter&template=image-porter.md&title=%5BPORTER%5D) ,将自动触发 github actions 进行拉取转推到docker hub

>注意：
>为了防止被滥用，目前仅仅支持一次同步一个镜像
>Issues 必须带 `porter` label
>标题必须为 `[PORTER]镜像名:tag` 的格式，例如`[PORTER]k8s.gcr.io/pause:3.6`

issues的内容无所谓，可以为空

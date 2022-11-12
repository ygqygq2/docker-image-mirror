# 镜像仓库转换

- 默认推送到本人仓库： https://hub.docker.com/u/ygqygq2
- 如果源镜像 tag 中支持多架构，也会推送多架构镜像

Uses/如何拉取新镜像
-------
[创建issues](https://github.com/ygqygq2/docker-image-mirror/issues/new?assignees=&labels=porter&template=image-porter.md&title=%5BPORTER%5D) ,将自动触发 github actions 进行拉取转推到docker hub

>注意：
>为了防止被滥用，目前仅仅支持一次同步一个镜像    
>Issues 建议带 `porter` label 
>标题建议为 `[PORTER]镜像名:tag` 的格式，例如`[PORTER]k8s.gcr.io/pause:3.6`    

issues的内容设定为`skopeo copy`的参数，默认为空

其它参数可以参考：[skopeo copy](https://github.com/containers/skopeo/blob/main/docs/skopeo-copy.1.md)

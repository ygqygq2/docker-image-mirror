# 镜像仓库转换

- 推送到本人仓库： docker.io/ygqygq2
- 推送到阿里云仓库： registry.cn-hangzhou.aliyuncs.com/img_mirror
- 如果源镜像 tag 中支持多架构，也会推送多架构镜像
- 默认使用 skopeo 同步镜像，失败之后会使用 docker

如需要在大陆访问，请移步到 [mirror-images-to-harbor](https://github.com/linuxba/mirror-images-to-harbor) 提 issue 同步镜像，镜像存在本人私有仓库，公开镜像保存 5 个 tag；

## Uses/如何拉取新镜像

[创建 issues](https://github.com/ygqygq2/docker-image-mirror/issues/new?assignees=&labels=porter&template=image-porter.md&title=%5BPORTER%5D) ,将自动触发 github actions 进行拉取转推到 docker hub

> 注意：
>
> - 为了防止被滥用，目前仅仅支持一次同步一个镜像
> - Issues 建议带 `porter` label
> - 标题建议为 `[PORTER]镜像名:tag` 的格式，例如`[PORTER]k8s.gcr.io/pause:3.6`

issues 的内容设定为`skopeo copy`的参数，默认为空

其它参数可以参考：[skopeo copy](https://github.com/containers/skopeo/blob/main/docs/skopeo-copy.1.md)

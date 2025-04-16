# HPCesia/1Panel-Apps

简体中文 | [English](./README.en.md)

我个人制作的 [1Panel](https://github.com/1Panel-dev/1Panel) 应用的仓库。

## 使用方式

下载源码到本地后将需要的应用上传到服务器的 `/opt/1panel/resource/apps/local` 目录（默认安装目录）下，或直接在服务器上使用下面的代码：

```sh
git clone https://codeberg.org/HPCesia/1panel-apps.git /opt/1panel/resource/apps/local/1panel-apps # Codeberg，中国大陆地区可用，稳定
# git clone https://github.com/HPCesia/1panel-apps.git /opt/1panel/resource/apps/local/1panel-apps # GitHub 镜像，中国大陆地区不可用，稳定
# git clone https://repo.hpcesia.com/HPCesia/1panel-apps.git /opt/1panel/resource/apps/local/1panel-apps # 自建 Forgejo 镜像，中国大陆地区可用，不稳定
cp -rf /opt/1panel/resource/apps/local/1panel-apps/apps/* /opt/1panel/resource/apps/local/
rm -rf /opt/1panel/resource/apps/local/1panel-apps
```

## 软件列表

| 名称                      | 仓库版本 |
| ------------------------- | -------- |
| Authelia                  | 4.38.17  |
| Forgejo                   | 10.0.3   |
| Koishi                    | 1.15.0   |
| Syncthing Discover Server | 1.28.0   |

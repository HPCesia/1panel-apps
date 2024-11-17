# HPCesia/1Panel-Apps

## 简介

我个人制作的 [1Panel](https://github.com/1Panel-dev/1Panel) 应用的仓库，由于各种原因没有 PR 到[官方仓库](https://github.com/1Panel-dev/appstore)或[第三方仓库](https://github.com/okxlin/appstore)的应用都会放到这里。

## 使用方式

下载源码到本地后将需要的应用上传到服务器的 `/opt/1panel/resource/apps/local` 目录（默认安装目录）下，或直接在服务器上使用下面的代码：

```sh
git clone https://github.com/HPCesia/1pnel-apps /opt/1panel/resource/apps/local/1pnel-apps
# git clone https://gitea.hpcesia.com/HPCesia/1pnel-apps /opt/1panel/resource/apps/local/1pnel-apps # 自建 Gitea，中国大陆地区可用，不稳定
cp -rf /opt/1panel/resource/apps/local/1pnel-apps/apps/* /opt/1panel/resource/apps/local/
rm -rf /opt/1panel/resource/apps/local/1pnel-apps
```

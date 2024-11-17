## 简介
Authelia 是一个开源的身份验证和授权服务器，它通过 Web 界面提供应用程序的两因素认证（2FA）和单点登录（SSO）。它作为反向代理的伴侣，能够允许、拒绝或重定向请求。

更多信息请参阅[官方文档](https://www.authelia.com/)。

## 配置
安装完成后，请到应用目录的 `data` 目录下修改 `configuration.yml` 与 `users_database.yml` 修改配置。

本版本为 `lite` 版本，适用于个人轻量使用环境，不依赖其他任何服务。
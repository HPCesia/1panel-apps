## 简介

Authelia 是一个开源的身份验证和授权服务器，它通过 Web 界面提供应用程序的两因素认证（2FA）和单点登录（SSO）。它作为反向代理的伴侣，能够允许、拒绝或重定向请求。

更多信息请参阅[官方文档](https://www.authelia.com/)。

## 配置

本应用分为 `lite` 版本与全量版本（尚未制作），`lite` 版本适用于个人轻量使用环境，不依赖其他任何服务，资源消耗少；全量版本适用于较大规模的服务，需要部署 LDAP、PostgreSQL、Redis。

安装完成后，请到应用目录的 `data` 目录下修改 `configuration.yml` 进行配置，`lite` 版本还需修改 `users_database.yml`。

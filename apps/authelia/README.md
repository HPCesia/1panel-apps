## 简介

Authelia 是一个开源的身份验证和授权服务器，它通过 Web 界面提供应用程序的两因素认证（2FA）和单点登录（SSO）。它作为反向代理的伴侣，能够允许、拒绝或重定向请求。

更多信息请参阅[官方文档](https://www.authelia.com/)。

## 配置

本应用分为 `lite` 版本与全量版本（尚未制作），`lite` 版本适用于个人轻量使用环境，不依赖其他任何服务，资源消耗少；全量版本适用于较大规模的服务，需要部署 LDAP、PostgreSQL、Redis。

安装完成后，请到应用目录的 `data` 目录下修改 `configuration.yml` 进行配置，`lite` 版本还需修改 `users_database.yml`。

### 机密配置
目前版本中，机密均位于 data/secrets 目录下，**所有 secrets 目录下的文件均需要进行修改！**

#### 机密清单
- `STORAGE_ENCRYPTION`：应为不低于 20 位的随机字符串
- `SESSION_SECRET`：应为不低于 64 位，且仅包含大小写字母与数字的随机字符串
- `JWT_SECRET`：应为不低于 64 位，且仅包含大小写字母与数字的随机字符串
- `HMAC_SECRET`：应为不低于 64 位，且仅包含大小写字母与数字的随机字符串
- `oidc/jwks/rsa.2048.key` 与 `oidc/jwks/rsa.2048.key.pub`：应为使用 RSA 方法生成的、位数不低于 2048 的一对公私钥

#### 设置方法
所有机密均可使用 Authelia 进行生成。可以通过打开 1Panel 中应用对应容器的终端使用，或者记下容器名称，在 ssh 连接到服务器后，使用 `docker exec -it 1Panel-xxxxx /bin/sh` 进入应用对应容器的终端。

- 随机字符串：
  ```bash
  authelia crypto rand --length 64 --charset alphanumeric
  ```
- RSA 密钥对：
  ```bash
  authelia crypto pair rsa generate --directory /config/secrets/oidc/jwks --file.private-key rsa.2048.key --file.public-key rsa.2048.key.pub
  ```
# HPCesia/1Panel-Apps

[简体中文](./README.md) | English

A personal repository of [1Panel](https://github.com/1Panel-dev/1Panel) applications.

## Usage

After downloading the source code locally, upload the desired applications to the `/opt/1panel/resource/apps/local` directory (default installation directory) on your server, or directly use the following code on your server:

```sh
git clone https://codeberg.org/HPCesia/1panel-apps.git /opt/1panel/resource/apps/local/1panel-apps # Codeberg, stable
# git clone https://github.com/HPCesia/1panel-apps.git /opt/1panel/resource/apps/local/1panel-apps # GitHub mirror, stable
# git clone https://repo.hpcesia.com/HPCesia/1panel-apps.git /opt/1panel/resource/apps/local/1panel-apps # Self-hosted Forgejo mirror, unstable
cp -rf /opt/1panel/resource/apps/local/1panel-apps/apps/* /opt/1panel/resource/apps/local/
rm -rf /opt/1panel/resource/apps/local/1panel-apps
```

## Application List

| Name                      | Version |
| ------------------------- | ------- |
| Authelia                  | 4.38.17 |
| Forgejo                   | 10.0.3  |
| Koishi                    | 1.15.0  |
| Syncthing Discover Server | 1.28.0  |

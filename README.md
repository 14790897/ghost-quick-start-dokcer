## 使用方法

复制 .env docker-compose.yml 到同一目录下
修改域名, 数据库密码,邮件配置后使用 docker compose up -d 启动

simple_caddyfile.conf 作为 caddy 的配置文件
修改域名后将其内容复制到 /etc/caddy/Caddyfile 然后重启 caddy 服务: sudo systemctl restart caddy

## 参考:

https://github.com/TryGhost/ghost-docker

https://docs.ghost.org/install/docker#setup-your-config

更新.env 后使用 docker compose up -d --force-recreate ghost 应用

ghost 不能和 warp 代理一起使用 邮件会被阻断 有时无法访问

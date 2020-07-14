# docker-shadowsocks-libev
Shadowsocks libev image with obfs.

https://github.com/shadowsocks/shadowsocks-libev

Latest Version: v3.3.4

Useage:

```yaml
version: '2'
services:
  shadowsocks:
    image: cquzc/shadowsocks-libev
    ports:
      - "10010:8388/tcp"
      - "10010:8388/udp"
    environment:
      - METHOD="xchacha20-ietf-poly1305"
      - PASSWORD="123456"
      - OBFS_OPTS="obfs=http;obfs-host=microsoft.com"
    restart: always
```

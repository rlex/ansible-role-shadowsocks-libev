### Ansible role for [shadowsocks-libev](https://github.com/shadowsocks/shadowsocks-libev)
Installs shadowsocks-libev from packages (available in deb8 backports, deb9 and ubuntu >= 17.10), and configures it.  
By default, configures shadowsocks-libev with simple http obfuscation

Configurable parameters (default ones):
```
shadowsocks_libev_packages:
  - shadowsocks-libev
  - simple-obfs
shadowsocks_libev_password: password
shadowsocks_libev_server: 0.0.0.0
shadowsocks_libev_server_port: 443
shadowsocks_libev_local_port: 3333
shadowsocks_libev_timeout: 1800
shadowsocks_libev_method: chacha20-ietf-poly1305
shadowsocks_libev_dns: 1.1.1.1
shadowsocks_libev_mode: tcp_and_udp
shadowsocks_libev_obfs: true
shadowsocks_libev_plugin: obfs-server
shadowsocks_libev_plugin_opts: obfs=http;fast-open
shadowsocks_libev_fast_open: true
```

For TLS obfuscation use something like
```
shadowsocks_libev_plugin_opts: obfs=tls;failover=127.0.0.1:8443;fast-open
```

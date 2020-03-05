# shadowsocks安装使用指南

## 自行下载安装
### 下载安装
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install python-pip
sudo apt-get install python-setuptools m2crypto
pip install shadowsocks
```
### 启动与关闭
```
sudo .local/bin/ssserver -c /home/tjc/ss-file/shadowsocks.json -d start
sudo .local/bin/ssserver -c /home/tjc/ss-file/shadowsocks.json -d stop
```

## 第三方脚本（开机自启动）

```
root用户下执行：
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh
chmod +x shadowsocksR.sh
./shadowsocksR.sh 2>&1 | tee shadowsocksR.log
wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && ./bbr.sh
reboot
sysctl net.ipv4.tcp_available_congestion_control
```

## 各种相关路径

```
配置文件路径：/etc/shadowsocks.json。
```
## 配置文件范例（多账号，ssr）

```
{
    "server":"0.0.0.0",
    "port_password":{
        "8888":"87654321",
        "9999":"12345678"
    },
    "timeout":120,
    "method":"aes-256-cfb",
    "protocol":"auth_aes128_sha1",
    "protocol_param":"123456789asdf",
    "obfs":"http_simple",
    "obfs_param":"123456789asdf",

    "fast_open":false,
    "workers":10
}
```
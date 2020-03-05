# linux用户操作

## 添加新用户
```
useradd -r -m -s /bin/bash tjc
passwd tjc
```
## 用户sudo权限
```
chmod +w /etc/sudoers
nano /etc/sudoers
添加一行 tjc ALL=(ALL:ALL) ALL
```
## 删除用户
```
userdel -r tjc
```
# linux虚拟内存swap配置

## 命令

```
删除swap交换缓存
sudo swapoff /swap
sudo rm /swap

新建swap缓存
sudo fallocate -l 4G /swap
sudo chmod 600 /swap
sudo mkswap /swap
sudo swapon /swap
sudo swapon -s
sudo nano /etc/fstab
最后添加一行 /swap none swap sw 0 0

查看内存空间大小：free -m
```
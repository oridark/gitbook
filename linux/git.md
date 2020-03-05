# git安装与免密操作

## 下载安装

```
sudo apt-get install git
```

## 配置用户信息

```
git config --global user.name "Your Name"
git config --global user.email Your_email@example.com
```
# 通过SSH连接Github
## 安装ssh

```
sudo apt-get install ssh
```
### 首先 ssh-keygen 会确认密钥的存储位置和文件名（默认是 .ssh/id_rsa）,然后他会要求你输入两次密钥口令，留空即可。所以一般选用默认，全部回车即可。
## 创建密钥文件
```
ssh-keygen -t rsa -C "你的github账号邮箱"
```
### 默认密钥文件路径在~/.ssh，id_rsa是私钥文件，id_rsa.pub是公钥文件
## 将公钥添加到Github
```
1，将id_rsa.pub文件内容全部复制
2，登陆到GitHub上，右上角小头像->Setting->SSH and GPG keys中，点击new SSH key。
```
## SSH测试
```
1，将id_rsa.pub文件内容全部复制
2，登陆到GitHub上，右上角小头像->Setting->SSH and GPG keys中，点击new SSH key。
```
### 如果结果为 “ ...You've successfully authenticated, but GitHub does not provide shell access”，则说明成功。
## 设置远程仓库
```
git remote add origin git@github.com:Username/Repositories_Name.git
如果手误输错，可通过git remote remove origin命令删除该远程仓库。
```
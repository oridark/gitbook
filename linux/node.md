# node安装使用指南

## 下载安装nvm

```
sudo apt-get update
sudo apt-get install build-essential libssl-dev
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.1/install.sh | bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
nvm -v // 验证是否安装成功
nvm ls-remote // 查看可安裝的 Node.js 版本
nvm install v11.15.0 // 安裝指定版本
nvm ls // 查看已安裝版本
nvm use v11.15.0 // 使用已安装的指定版本
```

## 常用node与npm命令

```
node -v
npm -v
npm install -g xxx
npm config set registry https://registry.npm.taobao.org
npm config set proxy http://127.0.0.1:1080
npm cache clean --force

```
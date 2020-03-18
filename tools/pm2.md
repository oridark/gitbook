# pm2

## 下载安装pm2

```
npm install -g pm2

```

## 常用pm2命令

```
pm2 start xxxx --watch // 启动服务

pm2 restart all // 重启所有应用
 
pm2 save // 保存服务

pm2 update    // Save processes, kill PM2 and restore processes

pm2 resurrect   // 重新加载保存的应用列表
 
pm2 startup // 把已启动服务加到systemd中
  
pm2 unstartup systemd // 删除自动启动服务

pm2 logs [app-name]   // 显示指定应用程序的日志

pm2 flush    // 清空所有日志文件

pm2 stop all     // 停止所有的应用程序

pm2 stop 0    // 停止 id为 0的指定应用程序

```
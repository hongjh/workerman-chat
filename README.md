workerman-chat
=======
基于workerman的GatewayWorker框架开发的一款高性能支持分布式部署的聊天室系统。

GatewayWorker框架文档：http://www.workerman.net/gatewaydoc/

 特性
======
 * 使用websocket协议
 * 多浏览器支持（浏览器支持html5或者flash任意一种即可）
 * 多房间支持
 * 私聊支持
 * 掉线自动重连
 * 微博图片自动解析
 * 聊天内容支持微博表情
 * 聊天内容支持多种方式记录，文件、数据库
 * 支持多服务器部署
 * 业务逻辑全部在一个文件中，快速入门可以参考这个文件[Applications/Chat/Event.php](https://github.com/walkor/workerman-chat/blob/master/Applications/Chat/Event.php)   
  
下载安装
=====
1、git clone https://github.com/walkor/workerman-chat

2、composer install

3、配置.env文件

4、创建聊天记录表


配置
=====
聊天内容日志位置,注意权限问题，程序尝试自动创建该目录。

CHAT_LOG_DIR=./logs/ 

聊天内容日志保存类型，file:文件,mysql:mysql数据库，如果是 file 需要配置 CHAT_LOG_DIR (聊天记录保存目录)，如果是 myslq 需要配置数据库相关。

CHAT_LOG_TYPE=file

更多参见.env.example

启动停止(Linux系统)
=====
以debug方式启动  
```php start.php start  ```

以daemon方式启动  
```php start.php start -d ```

启动(windows系统)
======
windows版本请到这里下载，启动方式参考下面源码中README.md

https://github.com/walkor/workerman-chat-for-win/archive/master.zip

注意：  
windows系统下无法使用 stop reload status 等命令  
如果无法打开页面请尝试关闭服务器防火墙  

测试
=======
浏览器访问 http://服务器ip或域:55151,例如http://127.0.0.1:55151

 [更多请访问www.workerman.net](http://www.workerman.net/workerman-chat)

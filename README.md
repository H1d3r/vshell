# vshell
vshell 是一款go编写的rat 

文件都是二进制的，只是拿蚁剑进行主机控制

基本框架为

client <-> teamserver <-> 蚁剑

目前仅支持 TCP TLS反连上线的模式
![](img/README/2021-09-23-11-43-00.png)

client

![](img/README/2021-09-23-11-44-54.png)

teamserver
![](img/README/2021-09-23-11-44-31.png)

功能：
1.蚁剑马的所有已有功能（文件上传/下载、命令执行、数据库操作、修改文件时间戳等。。。）
命令执行
![](img/README/2021-09-21-18-11-15.png)
文件操作
![](img/README/2021-09-21-18-11-43.png)

数据库操作
![](img/README/2021-09-21-18-13-09.png)
![](img/README/2021-09-21-18-13-59.png)
2.屏幕截屏

![](img/README/2021-09-24-15-31-15.png)

3.获取LSASS进程文件，导入mimikatz

4.端口复用，上线即代理

机器上线会在teamserver创建一个端口，这个端口既是蚁剑的连接端口，又是socks5代理端口（花了很久的时间才完成的端口复用）

且teamserver和client的连接都是TLS加密的，自然socks5的包也会被加密

![](img/README/2021-09-23-11-38-30.png)


![](img/README/2021-09-23-11-36-28.png)

甚至，你可以使用蚁剑控制手机

![](img/README/2021-09-24-15-48-50.png)
![](img/README/2021-09-24-15-49-23.png)
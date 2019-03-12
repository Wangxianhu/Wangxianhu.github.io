---
layout:     post
title:      "linux常用shell命令"
subtitle:   " \"一些简单常用shell命令的记录\""
date:       2019-03-12 9:00:00 UTC+8
author:     "王先虎"
header-img: "img/about-markdown/bg.jpg"
tags:
    - linux
    - 学习
    - 笔记
---

由于自己不是做运维的，但是工作有打包上传项目，解决一些简单服务器问题的需要，所以简单linux shell命令是需要的，这里只是一些简单的记录，以后如有需要再在原文上添加

## 1、查询当前下目录文件及文件夹命令
	
快速查询

``` shell
ll
``` 

## 2、进入目录命令

进入命令和dos命令类似都是cd

``` shell
cd a文件夹/b文件加
```

## 3、删除文件命令

``` shell
rm -fr 文件或文件加
```

## 4、上传文件

上传文件一般都是用ssh软件连接服务器，用ssh上传

## 5、启动关闭tomcat

启动关闭tomcat一般都是执行bin文件夹下的sh命令

启动命令

``` shell
sh bin/startup.sh
```

关闭命令

``` shell
sh bin/shutdown.sh
```

## 6、查看启动日志

查看日志实际上就是查看文件，实际上就是查看logs路径下的catalin.out文件，查看命令是tail

``` shell
tail logs/catalina.out
```

## 7、查杀进程命令

查进程用ps（会查出进程号），杀进程用kill，就以查杀tomcat为例

查进程

``` shell
ps -ef |grep tomcat
```

杀进程

``` shell
kill -9 进程号
```
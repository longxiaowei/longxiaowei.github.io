---
layout: post
title:  "windows中安装mysql-8.0.14"
date:   2019-01-29
tags: longxiaowei
color: rgb(255,90,90)
cover: '../assets/blogimg/2018-10-24.png'
subtitle: 'windows中安装mysql-8.0.14步骤记录'
---
# windows中安装mysql-8.0.14步骤记录

- 下载mysql 安装包

- 解压并进入安装目录 
	
	<img src="/assets/blogimg/2018-10-21.png">

- 配置path环境变量

- 初始化服务信息
	
	- 在mysql安装目录下 即bin文件夹同级 新建 data文件夹和my.ini文件,my.ini内容如图，用window记事本打开保存，ANSI编码。

	- 以管理员的身份打开cmd窗口 初始化服务：
	mysqld --initialize --user=mysql --console
	初始化完成之后，会生成一个临时密码,将此密码复制保存


- 安装服务

	mysqld -install

- 启动服务

	net start mysql

- 修改密码 

	mysql -u root -p登录数据库 输入上面的临时密码

	ALTER USER root@localhost IDENTIFIED  BY '123456'; 将密码为123456

[jekyll-docs]: https://www.baidu.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

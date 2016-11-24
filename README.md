# build-your-own-docker
自己动手写Docker。 重复造轮子，初步定位是可以写一个能够类似于runc 一样的容器运行引擎，然后加上资源的隔离。最好能有image的支持，希望做出一个最简版的docker，帮助自己和感兴趣的同学深入理解 docker 的原理以及具有动手实践案例。

## 目录
- 前言
- 为什么写这本书
	
- 准备工作
	- 安装Golang
	- Golang Hello World
	
- Docker 简介
	- 什么是 Docker
	- Docker 主要使用了哪些技术

- 基础技术介绍
	- [Linux Namespace](1/1.1.md)
  		- 概念
  		- UTS Namespace
  		- IPC Namespace
  		- PID Namesapce
  		- Mount Namespace
  		- User Namesapce
  		- Network Namespace
  		- 小结  		  
	- Linux Cgroups
  		- 什么是Linux Cgroups
  		- Docker 中哪里使用了Cgroups
  		- 自己动手写Cgroups 例子

  	- Union File System
  		- 什么是Union File System
  		- Docker 哪里使用了UFS
  		- 自己动手写UnionFS 例子

- 构造简单容器
	- 使用Namespace 创建隔离的容器
		- PID 隔离的容器
		- UID 用户隔离
		- Network 隔离
		- Mount 隔离
	- 使用Cgroups 限制容器资源使用
		- Memory 限制
		- CPU 限制
	- 使用Union FS挂载外部路径
		- AUFS 挂载
		- Overlay FS 挂载
		- DeviceMapper 挂载

- 构造镜像 
	- 构造一个简单的镜像
		- 手工创建Linux 基本镜像
		- 打包镜像
		- 使用基本镜像创建容器

- 配置容器网络
	- 配置local bridge
 	- 使用本地网桥使容器与host 通信
 	- 实现容器之间的通信


- 创建Daemon Server
	- 构建一个API server
	- 使用API server 创建容器

- 镜像存储
	- 使用oss 存储镜像
	- 实现pull 拉取镜像

- 总结
	- 完整的根据镜像构建一个网络挂载点隔离的容器
	- 说明一下各个部分对应的docker 模块
	- 概述docker 各个模块关系
	- 展望
 	
## 作者列表
- 陈显鹭 (阿里云容器服务团队)
- 王炳燊 (阿里云容器服务团队)
- 秦妤嘉 (阿里云容器服务团队)

## License
Book License: [CC BY-SA 3.0 License](https://creativecommons.org/licenses/by-sa/3.0/)

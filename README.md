# build-your-own-docker
自己动手写Docker。 重复造轮子，初步定为是可以写一个能够类似于runc 一样的容器运行引擎，然后加上资源的隔离。最好能有image的支持，希望做出一个最简版的docker，帮助自己和感兴趣的同学深入理解 docker 的原理以及具有动手实践案例。

# 目录
- 介绍Linux Namespace
  - 什么是Linux Namespace
  - 如果利用Golang 写一个简单的Namespace 隔离进程的小例子
  
- 介绍Linux Cgroups
  - 什么是Cgroups
  - 利用Cgroups 写一个简单的Demo 来限制进程的资源利用
  
- 根据Runc spec 定义的格式来创建一个容器

# License
Book License: [CC BY-SA 3.0 License](https://creativecommons.org/licenses/by-sa/3.0/)

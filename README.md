# ebook

# 前言
介绍编写本书初衷，包括什么内容，本书不具备什么内容，适用读者，勘误表地址、联系方式。

# (第一部分 基础概念篇)

# 第1章 嵌入式Linux基础概念
介绍嵌入式Linux是什么，由哪些部分构成，该怎么学  
## 1.1 嵌入式Linux是什么
## 1.2 嵌入式Linux由哪些部分组成
## 1.3 如何学习嵌入式Linux
## 1.4 本书代码示例说明
（使用ubuntu+qemu，另在实际板子(s3c2440或rk3188)上运行）
## 1.5 本书实验平台说明
## 1.6 本章小结

# (第二部分 系统系统篇)

# Linux系统的安装——基于Ubuntu16.04
## 使用虚拟机VMware Workstation安装Ubuntu
（图解安装过程，添加说明）
## 安装Ubuntu后要做的配置
（分类说明要安装的软件及作用）

# Linux系统使用
## Linux系统目录
### Linux目录结构介绍
### /proc目录、/sys目录
（与后面内核驱动开发有关联）
## Linux命令
### 编辑器相关命令
### 编译相关命令
### 系统相关命令
### 其它命令
### man命令
### 命令使用经验
## shell使用
## 系统配置
（环境变量、/etc/文件配置（issue显示字符串、主机别名(lserver)））
## 更新Linux内核
### 深入掌握Linux结构
（LFS、debootstrap）
## 扩展思考
（讲如何慢慢积累命令行）
## 本章小结

# 嵌入式Linux开发环境搭建
## 嵌入式Linux开发概述
（描述编写代码、编译代码、运行代码过程） 
## Windows系统所需工具
### 综合类
### 编辑类
### 连接工具类
（source insight、notepad++、secureCRT）
## Linux系统所需服务
（前面已经安装好Linux系统）
### SSH
### Samba
### NFS
### FTP
### Telnet
## 扩展思考
## 本章小结
（固定好IP地址，设置好这些服务，本书一直会使用）

# （第三部分 Linux应用开发篇）

# 版本管理工具git
（说明为什么要使用git，本书代码、勘误也使用git。  
公司会使用，多人协作  
个人日常学习也可以使用  
每个应用命令，都使用windows工具和linux命令行
）
## 版本管理工具概述
(重要性、必要性、本章术语约定）  
## git应用场景
（本地仓库、远程仓库）  
## Windows系统下TortoiseGit的安装
## Linux系统下Git的安装
## 入门使用
（填写账号和邮箱，建立仓库、克隆仓库、提交仓库、查看修改、撤销修改）  
## Linux系统下Git服务器搭建
### Git服务器搭建过程
### Git权限控制
### 使用ssh密钥登陆Git服务器
### 使用账号密码登陆Git服务器
## 分支
### 创建分支
### 冲突及冲突解决
### 分支管理
## 标签
## 远程仓库
### 添加远程仓库
### 克隆远程仓库
### 推送到远程仓库
## 其它用法
### 忽略指定文件和目录
### 子仓库
### Git命令别名
## 国内外常见的Git托管网站
github gitlab bitbucket gitee
## Git应用实践经验
（介绍个人实际使用Git的经验）
## 扩展思考
（自行搭建本地gitlab仓库、参与github开源项目、使用Gerrit）
## 本章小结

# Linux系统自动化编译和Makefile
## Linux下工具、库编译方法
### 下载源码
### 编译三步曲
### 编译配置实例
## autotool工具集
（参考http://www.linuxprobe.com/system-gnu-autotool.html ）  
## 安装交叉编译器
### 直接使用现成的交叉编译器
### 自行制作交叉编译器
## Makefile
### Makefile基础知识
（介绍makefile基础内容）
### 在Makefile中执行shell命令
### Makefile模板实例
## 扩展思考
## 本章小结

# 二进制工具
## 概述
## gcc工具链
### ar
### nm
### strings
### strip
### objcopy
### readelf
## ELF格式
## 扩展思考
## 本章小结

# 应用程序开发
## 概述
## 编程规范
### 编码风格
原则：入乡随俗
### 编程原则
## Linux应用层模块分类
### 多进程编程
### 多线程编程
### 串口编程
## helloworld全面追踪
## 扩展思考
## 本章小结

# 调试手段
## 使用printf打印跟踪
注：日志系统
## 消除gcc编译警告
注：从代码源码把控  
## 利用coredump文件调试
## 扩展思考
## 本章小结

# (第四部分 嵌入式Linux移植篇)

# 嵌入式Linux移植总览
## 学习所需技能
## 如何阅读芯片手册
## 宿主机与目标板共享的几种方式
### NFS
### SSH
### FTP
### 硬件介质：U盘和SD卡
## 扩展思考
## 本章小结

# bootloader移植
## u-boot
### u-boot概述
### u-boot在qemu环境的启动
注：给出启动流程图
### 在u-boot中新加命令
### u-boot进程空间示例
## coreboot
### coreboot概述
### coreboot在qemu环境的启动
## 扩展思考
## 本章小结

# Linux内核移植
## 内核配置编译步骤
（与x86平台更新的联系和区别）  
## 内核编译常见错误
## 内核配置(menuconfig)选项说明
## 内核Makefile与Kconfig文件
## 添加自定义驱动
### 将驱动编译进内核
### 将驱动编译为ko文件：独立目录
### 将驱动编译为ko文件：使用内核目录
## 内核移植实践经验
注：厂商提供有BSP包，直接使用
## 扩展思考
## 本章小结

# rootfs移植
## rootfs概述
## busybox
（注意说明与前面的linux目录的联系和差异）
### busybox编译
## 制作ramdisk镜像
## 在qemu挂载rootfs
## 扩展思考
（描述其它格式的images制作）
## 本章小结

# Linux驱动开发
注：注意说明与前面章节的区别
## 驱动分类概述
## 配合芯片手册阅读代码
示例：WDT、RTC  
## platform设备驱动模板
## platform设备驱动流程跟踪
## 字符设备驱动流程跟踪
注：使用open、write、read、close、ioctl接口  
## GPIO驱动
## 异步通信驱动示例
## 户空间与内核空间之间的交互方式
### sys文件系统
### proc文件系统
注：sys、proc文件系统驱动示例  
## 扩展思考
## 本章小结

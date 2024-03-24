---
title: "FUXA SCADA安装"
date: 2024-03-24T18:02:54+08:00
#lead:    # 导言
description: ""
tags:
    - FUXA
    - SCADA
categories:
    - NTECHNOLOGY
---

FUXA是一个在GitHub上开源SCADA系统。可用来实现对机器和实时数据的可视化。

<!--more-->

## 安装并运行
**首先，介绍一点儿在命令行中操作的技巧：**
```
同盘操作：
    cd 下一级文件夹名称                    # 进入下一级目录
    cd 下一级文件夹名称/下下级文件夹名称    # 进入下下级文件夹

    cd ..       # 返回上一级目录
```
```
不同盘操作：
    D:          # 切换到D盘根目录
```

### 安装
软件的下载依据电脑操作系统。

1. 安装 **[Node](https://nodejs.org/en/download)**。
    * 安装目录可以保持默认，本次修改为了`C:\nodejs`。
    * npm是Nodejs下的包管理器，安装node时将连带安装。
    * 安装过程中会自动下载一些必要的软件。
    
    >node版本请选择`v16.20.2`，较新的版本目前不兼容FUXA

    安装完成后，在命令行中输入`node -v`查询是否安装成功；输入`echo %PATH%`，查看输出中是否自动添加了nodejs环境变量；输入`npm -v`查看npm是否安装成功。



1. 安装 **[FUXA](https://github.com/frangoteam/FUXA)**。

   * 安装FUXA有多种方法，可参考官方说明。本次采用下载压缩包并解压再用npm安装的方式。
   ```
    cd ./server     # 进入到FUXA解压后的server文件夹
    npm install     # 键入此命令进行安装
    npm start       # 键入此命令启动
   ```
    * 在浏览器输入键入`npm start`命令返回的网址，进入FUXA
    
        停止，暂时用的`Ctrl + c`

### 运行
* 打开Chrome浏览器，进入地址`http://localhost:1881`。

* FUXA 由两个不同的视图组成：
    1. 最终用户可视化:`http://localhost:1881/home`

    2. 项目和设计编辑器:`http://localhost:1881/editor`

## 使用
**[FUXA Wiki](https://github.com/frangoteam/FUXA/wiki)**

### 连接设备并配置标签

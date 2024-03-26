---
title: "MySQL（一）数据库操作"
date: 2024-03-24T09:18:51+08:00
#lead:   # 导言
description: ""
tags:
    - SQL
    - python
categories:
    - NOTE
---

操作MySQL建立数据库。

<!--more-->


## 数据库操作

### 链接数据库
    mysql -uroot -p
    mysql -uroot -mysql

### 退出数据库
    exit/quit/ctrl+d

>注意：SQL语句最后需要有分号`；`作为结尾

### 显示数据库版本
    select version();

### 显示时间
    select now();

### 查看所有数据库
    show database;

### 创建数据库
    create database 数据库名 charset=utf8;
    create database python04;
    create database python04 charset=utf8;

### 查看创建数据库的语句
    show create database ....
    show create database python04;

### 查看当前使用的数据库
    select database();

### 使用数据库
    use 数据库的名字
    use python04new;

### 删除数据库
    drop database 数据库名；        -- 删库跑路就用这个
    drop database python04;


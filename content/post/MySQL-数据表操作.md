---
title: "MySQL（二）数据表操作"
date: 2024-03-24T09:38:51+08:00
#lead:    # 导言
description: ""
tags:
    - SQL
    - python
categories:
    - NOTE
---


数据表的增删改查是最常用的。

<!--more-->

## 数据表的操作
### 查看表结构的详细信息
    desc 数据表的名字;
    desc xxxx;

    PS：desc是describe的缩写；该语句将显示表中各列的名称及属性

### 查看当前数据库中所有表
    show tables;

### 创建表：classes表（id 、name）
    create table 数据表名字 （字段1 类型 约束, 字段2 类型 约束）;

    create table xxxx(id int, name varchar(30));
    create table yyyy(id int primary key not null auto_increment, name varchar(30));

    可使用以下格式：
    create table yyyy(
        id int primary key not null auto_increment,     #字段1=id；类型=int；约束=主键，不为空
        name varchar(30)                                #字段2=name；类型=varchar，长度最大30
    );
* auto_increment 表示自动增长
*  not null 表示不能为空
*  primary key 表示主键
* default 默认值

#### 创建完成，查看表
    desc xxxx;

#### 创建students表（id、name、age、high、gender、cls_id）
    creat table students(
        id,
        name,
        age,
        high,
        gender,
        cls_id
    );

补充类型和约束：

    creat table students(
        id int unsigned not null auto_increment primary key,
        name varchar(30),
        age tinyint unsigned,
        high ,
        gender,
        cls_id
    );

#### 插入数据
    insert into students values(0, "老王", 18, 188.88, "男", 0);

#### 插入后，进行查询
    select * from students;     # 查询所有列

### 查看表的创建语句
    show create table 表名字;


### 修改表
* 添加字段
```SQL
    alter table 表名 add 别名 类型;
    eg.
    alter table students add birthday date; -- date类型，年月日
```
* 修改字段
    1. 重命名版
   ```SQL
   alter table 表名 change 原名 新名 类型及约束；
   eg.
   alter table students change birthday birth datetime not null;
   ```
   
    2. 不重命名版
   ```SQL
   alter table 表名 modify 列名 类型及约束;
   eg.
   alter table students modify birth date not null;
   ```

* 删除字段
  ```SQL
  alter table 表名 drop 列名;
  eg.
  alter table students drop birthday;
  ```

### 删除表
    drop table 表名;

    drop database 数据库;  # 删除数据库
    drop table 数据表;     # 删除数据表
    
    eg.
    drop table xxxx;       # 删除xxxx这个数据表



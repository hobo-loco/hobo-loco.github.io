---
title: "MySQL（三）数据的增删改查"
date: 2024-03-24T11:32:58+08:00
#lead:    # 导言
description: ""
tags:
    - SQL
    - python
categories:
    - NOTE
---
**增删改查(curd):**
创建(Create)、更新(Updata)、读取(Read) 和删除(Delete)

<!--more-->


### 增加
* 全列插入
```
    insert into 表名 valyes(...)
    主键字段可以用0、null、default来占位。
    eg.
    insert into classes valves(0,菜鸟班)；  # 向classes表中插入一个班级
    insert into students values(0, "小李飞刀", 20, "女", 1, "1990/1/1");    # 向students表中插入一个学生信息
 ``` 
>枚举(enum)中的下标从1开始。如：性别是一个枚举类型enum('男','女','中性')，则1=男、2=女

* 部分插入
```
    insert into 表名(列1,...) values(值1,...)
    insert into students (name, gender) values ("小乔",2);
```
>在部分插入时，数据表中约束为不许为空的列需要有

* 多行插入
```
    insert into students (name, gender) values ("小乔",2),("大乔",2);
```
### 修改
    update 表名 set 列1=值1,列2=值2... where 条件;
    update students set gender=1；                  #修改students表中所有行，将性别改为男
    update students set gender=1 where id=3;        #修改students表中id=3的那行，将性别改为男
    update students set age=22,gender=1 where id=3; #修改students表中id=3的那行，将年龄改为22、性别改为男

>**where 条件**，当某行满足该条件时，对这行进行修改

### 删除
* 物理删除

    真的删除，使用deiete
    ```
        delete frome 表名 where 条件;
        eg.
        delete frome students;                         #  删除students数据表
        delete frome students where name="小李飞刀";    # 删除students数据表中姓名为小李飞刀的行 
    ```

* 逻辑删除

    不是真的删除，使用update
  ```SQL
    -- 用一个字段来表示这条信息是否已经不再使用了。
    -- 给students表添加一个is_delete字段  bit  类型
    alter table students add is_delete bit default 0;
    update students set is_delete=1 where id=6;
  ```

### 查询基本使用
* 查询所有列
```
select * from 表名;
eg.
select * frome classes;               -- * 表示全部取出来
select * from students where id<9;    -- 取出id<9的行
```
* 查询指定列
```
select 列1,列2,... frome 表名;
eg.
select id,name frome classes;          # 查询classes表中id、name两列，输出结果只显示这两列
```
>可以使用as作为列或表指定别名，详见下↓
```
    select 字段1 as 别名1,字段2 as 别名2 from 数据表 where 条件;
    eg.
    select name as 姓名,gender as 性别 frome students;      # 查询students表中的name、gender两列；并使用姓名代替name、使用性别代替gender
```
**字段的顺序**：谁在前边就先显示谁，仍以上例解释：

    select gender as 性别,name as 姓名 frome students;
# postgreSql

参考[菜鸟教程-pgsql](https://www.runoob.com/postgresql/postgresql-tutorial.html)

## 连接数据库

```bash
    psql -U postgres -W
```
输入用户名登陆

## 查看数据库列表

```bash
    \l
```

## 新建数据库

```bash
    create database test
```
创建一个叫做``test``的数据库

## 查看用户

```PLSQL
    select * from pg_user;
```

## 新建用户

```PLSQL
    create user lmt with password '123456';
```

## 授权给用户

```PLSQL
    grant all privileges on database test to lmt;
```

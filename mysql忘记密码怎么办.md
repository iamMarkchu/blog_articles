## 概述
  很久不登服务器了，突然想新加一个数据库，发现忘记了root密码，很是蛋疼，之后，一顿google，百度，终于得到了解决。在这里记录一下通用的方案，以备不时之需。


## 操作步骤

### 你必须有服务器的root权限
  如果你没有服务器的权限，你怎么管理mysql进程？

### 修改mysql的配置文件
  找到 `/etc/mysql/my.cnf`文件，在里面加上两行代码
```
  	[mysqld]
	skip-grant-tables
```


### 无密码启动mysql

``` bash
/etc/init.d/mysql restart
```

### 执行下列语句

``` sql
use mysql;

-- 5.7版本
update user set authentication_string=PASSWORD("new password") where user='root';
-- 5.6及以下版本
update user set password=PASSWORD("new password") where user='root';

flush privileges;
```

### 还原mysql的配置文件
 去掉刚才修改的 `my.cnf`中的配置

### 重启mysql
``` bash
/etc/init.d/mysql restart
```

### 记牢新改的密码
拿个小本本记住吧！！！

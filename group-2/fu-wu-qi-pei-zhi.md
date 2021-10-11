# 服务器配置

1. 安装MySQL
2. 添加远程用户访问权限

```
# root表示mysql的一个用户名  '%'表示所有远程ip  '123456'是密码
# 该命令的意思是任何公网IP的都可以通过用户名为root 密码为123456 访问改数据库
grant all privileges on *.* to root@'%' identified by '123456' with grant 
option;

# 使其立即生效
flush privileges;

# 退出
exit;

# 重启mysql服务
service mysql restart
```

1. 防火墙中开放窗口

4.阿里云开放窗口

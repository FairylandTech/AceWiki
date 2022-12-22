# 订阅和管理(dnf/yum源)

**在目标服务器使用root用户执行**

## 官方订阅

[RedHat官方订阅参考文档](https://www.cnblogs.com/alicehome/p/15214197.html)

## epel-Release订阅

[epel-release官方文档](https://docs.fedoraproject.org/en-US/epel/)

# 优化.bashrc

```
# 修改文件 vim ~/.bashrc
alias vi='vim'
alias ls='ls -a --color=auto'
alias ll='ls -allh --color=auto'
```

# 普通用户添加到sudo

**在目标服务器使用root用户执行**

1. 添加sudoers写的权限
1. 修改sudoers文件
1. 还原sudoers文件权限

```
# 添加sudoers写的权限
chmod 640 /etc/sudoers
# 修改sudoers文件
vim /etc/sudoers
# 添加内容格式
# 用户名 ALL(ALL) ALL
# 还原sudoers文件权限
chmod 440 /etc/sudoers
```

# 关闭SELINUX

**在目标服务器使用root用户执行**

```
# 修改配置文件 /etc/selinux/config
vim /etc/selinux/config
# 注释 SELINUX=enforcing 并添加
SELINUX=disabled
# 重启后生效
reboot
```


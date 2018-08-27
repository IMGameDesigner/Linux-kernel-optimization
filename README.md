[一 内核]//One kernel
===================================

查看全部内核设置：//View all kernel settings:
-----------------------------------

>#sudo sysctl -a

查看某指定内核设置：//View a specified Kernel Setting:
----------------------------------------

>#sudo sysctl -a|grep [name substring]

（例如查看net.ipv4.tcp_rmem ：）//For example, look at net.ipv4.tcp_rmem

>#sudo sysctl -a|grep tcp_rmem

（例如查看内核名中包含tcp的所有内核设置 ：）//For example, see all kernel settings that contain TCP in the kernel name.

>#sudo sysctl -a|grep tcp

修改内核设置：//Modify kernel settings:
----------------------------------------

>#sudo vi /etc/sysctl.conf


>a（vi内部命令）//vi internal command


>net.ipv4.tcp_rmem=4000 80000 6000000（添加此行）//Add this line


>net.core.netdev_max_backlog=10000（添加此行）//Add this line


>esc（vi内部命令）//vi internal command


>:wq（vi内部命令）//vi internal command


>sysctl -p


[二 ulimit]//two ulimit
=======================================

查看ulinit所有配置：//View all configuration of ulinit:
----------------------------------------
>#ulimit -a

查看ulimit某个配置(以-n为例)：//View a configuration of ulimit (take -n for example):
----------------------------------------
>#ulimit -n 

修改ulimit某个配置(以-n为例)://Modify a configuration of ulimit (take -n for example):
----------------------------------------

>#ulimit -n 4096


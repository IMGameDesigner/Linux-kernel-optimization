内核
===================================
查看全部内核设置：
>#sudo sysctl -a
----------------------------------------
查看某指定内核设置：
>#sudo sysctl -a|grep [name substring]
（例如查看net.ipv4.tcp_rmem）
>#sudo sysctl -a|grep tcp_rmem
（例如查看内核名中包含tcp的所有内核设置）
>#sudo sysctl -a|grep tcp
----------------------------------------
修改内核设置：
>#sudo vi /etc/sysctl.conf
>a
(添加内核，如）
>net.ipv4.tcp_rmem=4000 80000 6000000
>net.core.netdev_max_backlog=10000
>esc
>:wq
>sysctl -p
----------------------------------------
查看ulinit所有配置：
>#ulimit -a
查看ulimit某个配置：
>#ulimit -n 
修改ulimit某个配置:
>#ulimit -n 4096
----------------------------------------
2018.8.27 11:04

#### 1.ssh登录输入以下指令（ensxxx改成自己对应的）   
```
vi /etc/sysconfig/network-scripts/ifcfg-ensxxx
```
#### 2.修改部分参数   
```
bootproto=static
```
设置网卡获得ip地址的方式，可选的选项有`static`、`dhcp`、`bootp`，分别对应静态指定的ip地址，通过dhcp协议获得的ip地址，通过bootp协议获得的ip地址。
```
onboot=yes
```
系统启动时是否设置此网络接口，如果为`no`就改为`yes`即可。设置为yes时，表示网卡设备自动启动系统启动时激活此设备。   
#### 3.增加部分参数
```
#静态ip地址
IPADDR=192.168.31.9
#子网掩码
NETMASK=255.255.255.0
#网关
GATEWAY=192.168.31.1
#DNS
DNS1=114.114.114.114
DNS2=223.5.5.5
```
#### 4.重启网络  
```
service network restart
```

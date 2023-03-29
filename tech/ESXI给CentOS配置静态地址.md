1.ssh登录输入以下指令（ensxxx改成自己对应的）   
```
vi /etc/sysconfig/network-scripts/ifcfg-ensxxx
```
2.修改   
（1）bootproto=static   
#设置网卡获得ip地址的方式，可能的选项为static，dhcp或bootp，分别对应静态指定的 ip地址，通过dhcp协议获得的ip地址，通过bootp协议获得的ip地址    
（2）onboot=yes   
yes #系统启动时是否设置此网络接口，设置为yes时，系统启动时激活此设备   
新增   
IPADDR=192.168.3.60   
NETMASK=255.255.255.0   
GATEWAY=192.168.3.1   
DNS1=119.29.29.29   
DNS2=8.8.8.8   
3.重启网络  
```
service network restart
```

# ssr
支持Debian系统和Centos系统
安装完成后输入 ssr 即可使用本程序
#Debian系统用这个
apt install unzip wget
#or
#Centos系统用这个
yum install unzip wget 

wget https://raw.githubusercontent.com/mhl2020/ssr/master/ssr.zip && unzip ssr.zip && cd SSR* && bash install.sh

#*不是被屏蔽的，就这样，直接用

#秋水逸冰的单SSR脚本
wget --no-check-certificate https://linuxscript.oss-cn-shanghai.aliyuncs.com/qsyb-SSR/SSR.sh
chmod +x SSR.sh
./SSR.sh 2>&1 | tee shadowsocksR.log

#firewalld 服务基本使用
1、firewall 与 iptables 一样都是服务，所以可以使用 systemctl 服务管理工具来操作

目的	命令
查看防火墙状态	systemctl status firewalld

关闭防火墙，停止 firewall 服务	systemctl stop firewalld

开启防火墙，启动 firewall 服务	systemctl start firewalld

重启防火墙，重启 firewall 服务	systemctl restart firewalld

查看 firewall 服务是否开机启动	systemctl is-enabled firewalld

开机时自动启动 firewall 服务	systemctl enable firewalld.service

开机时自动禁用 firewall 服务	systemctl disable firewalld.service

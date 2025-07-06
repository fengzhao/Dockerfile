
Chrony是一个开源自由的网络时间协议 NTP 的客户端和服务器软软件。它能让计算机保持系统时钟与时钟服务器（NTP）同步，因此让你的计算机保持精确的时间，Chrony也可以作为服务端软件为其他计算机提供时间同步服务。

Chrony由两个程序组成，分别是chronyd和chronyc

chronyd是一个后台运行的守护进程，用于调整内核中运行的系统时钟和时钟服务器同步。它确定计算机增减时间的比率，并对此进行补偿。
chronyc提供了一个用户界面，用于监控性能并进行多样化的配置。它可以在chronyd实例控制的计算机上工作，也可以在一台不同的远程计算机上工作。

NTP 是网络时间协议（Network Time Protocol）的简称，通过 udp 123 端口进行网络时钟同步。

RHEL7中默认使用chrony作为时间服务器，也支持NTP，需要额外安装。NTP与chrony不能同时存在，只能用其中一个，并将另一个mask掉。



https://www.cnblogs.com/xzongblogs/p/14658895.html

```
210.72.145.44 国家授时中心
ntp.aliyun.com 阿里云
s1a.time.edu.cn 北京邮电大学
s1b.time.edu.cn 清华大学
s1c.time.edu.cn 北京大学
s1d.time.edu.cn 东南大学
s1e.time.edu.cn 清华大学
s2a.time.edu.cn 清华大学
s2b.time.edu.cn 清华大学
s2c.time.edu.cn 北京邮电大学
s2d.time.edu.cn 西南地区网络中心
s2e.time.edu.cn 西北地区网络中心
s2f.time.edu.cn 东北地区网络中心
s2g.time.edu.cn 华东南地区网络中心
s2h.time.edu.cn 四川大学网络管理中心
s2j.time.edu.cn 大连理工大学网络中心
s2k.time.edu.cn CERNET桂林主节点
s2m.time.edu.cn 北京大学
ntp.sjtu.edu.cn 202.120.2.101 上海交通大学


```

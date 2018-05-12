### ACL

***   
	access-list 1 permit 192.168.0.1 0.0.0.255   //创建标准访问列表 
	ip access-list extended plc-1-in  permit icmp 132.120.130.0  0.0.1.255  132.120.130.10 0.0.0.0  //创建扩展访问列表
> 

	ip access-group plc-1-in in //端口绑定
	no ip access-group plc-1-in //去除端口绑定
> 

	access-class 1 in //telnet口绑定
	no access-class 1 in //去除telnet口绑定
> 

	show ip access-list 1 //查看标准访问列表
	show ip access-list  plc-1-in //查看扩展访问列表

****
### 配置标准访问列表：
>access-list  列表号  permit/deny  源IP  源反转码

### 配置扩展访问列表：
>access-list extended acl名称 permit/deny 协议 源IP 源反转码 源端口 目的IP 目的反转码 目的端口

### 反转掩码
> - 反转掩码由四组八位二进制组成
> - **0意味着检查，1意味着忽略**

![反转掩码举例](https://i.imgur.com/rn3zyAb.png)

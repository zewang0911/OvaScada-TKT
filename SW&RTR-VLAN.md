## VLAN
1、查看vlan

	  sw1#show vlan brief
	  swi#show vlan vlan-id

2、在全局模式下配置vlan

	sw1(config)#vlan vlan-id     //添加一个vlan
	sw1(config-vlan)# name vlan-name  //给vlan取个名字

3、在vlan数据库创建vlan

	sw1#vlan database     //进入vlan数据库
	sw1(vlan)#vlan  vlan-id  name  qq  //添加一个vlan 名字为qq
	sw1(vlan)#exit

4、删除已创建的vlan

	sw1#vlan database
	sw1(vlan)# no vlan  vlan-id
或者 

	sw1(config)#no vlan 2

5、将端口加入到vlan

	sw1(config)#int f0/1      //进入端口模式
	sw1(config)# switchport mode access
	sw1(config-if)#switch access vlan vlan-id  //把端口加入到某个vlan
	sw1(config-if)#no switch access vlan vlan-id //将端口从某个vlan上删除
 
6、要同时把多个端口加入到某个vlan

	sw1(config)#int range  f0/0-10
	sw1(config-if-range)#switch access vlan vlan-id

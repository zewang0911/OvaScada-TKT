***
### 重新刷入配置文件


1、 擦除旧配置文件

	//擦除配置文件
	R1# erase startup-config
	//擦除配置文件二次确认
	Erase the nvram file system will remove all configuration files.Continue? <Enter>
	[ok]
	Erase of nvram:complete
	//重启路由器
	R1# reload
	Process with reload[confirm] <Enter>
	//不初始化配置对话框
	Would you like to enter the inital configurtion dialog[yes/no] no  

2、 写入配置文件。通过发送文本文件，若执行有问题可以分部分粘贴文件（平台：超级终端）

3、 写入到Startup-config中并且重新启动

	R1# write
	Building configuration [OK]
	R1# reload
	Process with reload[confirm] <Enter>

***
### running-config 和 startup-config

- flash:/ 放的是cisco的IOS系统文件
- nvram：/放的是启动时自动加载的配置文件，也就是startup-config
- system：/也就是交换机或路由器的内存ram，放的是当前运行的配置文件，即running-onfig

**copy running-config startup-config简写 copy run start把当前的配置文件保存在NVRAM中，以便下一次重启时可以用最新的配置文件，类似于存盘操作**
在特权模式下使用 dir flash:/ 可以查看IOS信息，同理可以查看其他存储介质内的信息
***
## 增加控制器步骤
1. 在Ovation Studio中将控制器授权成功
2. 获得主控制器的mac地址。链路正常，将主控制器上电，在error中获得主控制器的mac地址。
3. 获得辅控制器的mac地址。链路正常，将辅控制器上电，在error中获得辅控制器的mac地址
4. 在Ovation Studio中增加Drop15/65,启用n4
5. **配置device**
6. download_reboot
7. 建立类型为Drop类型Drop15，Drop65
8. Load
9. 在GB 1800上增加状态监视图形


***
**没有进行第五步操作，Drop15和Drop65均处于In control模式，下装等功能正常。解决办法如下：
两个控制器的内存卡格式化，按照正确步骤重新操作**  

----
格式化控制器内存卡：1g容量对应命令中16K，其他不同容量命令不一样  

    Format e: /a:16k /fs:fat  

存储卡装在控制器的左半边  

---
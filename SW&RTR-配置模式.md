### 配置模式
- 用户模式
>只能检测路由器或者交换机的配置  

      Router>             //用户模式
      Router> show arp   
      Router> show flash
- 特权模式
>可执行更多检测命令，可以调试路由器或者交换机

      Router>en           //进入特权模式
      Router#             //特权模式
      Router# show running config
      Router# exit        //退出到用户模式
      Router>            
- 全局配置模式
> 可以修改各项参数  

      Router> en          //进入特权模式
      Router# config t     //进入全局配置模式
      Router(config)#     //全局配置模式
      Router(config)# exit//退出到特权模式
      Router#             

- 接口模式
> 可以配置接口的参数 

      Router> en          //进入特权模式
      Router# config t     //进入全局配置模式
      Router(config)#     //全局配置模式
      Router(config)# fa0/0  //进入接口配置模式
      Router(config-if)#     //接口配置模式
      Router(config-if)# exit //退出到全局配置模式
      Router(config)# exit     //退出到特权模式
      Router#  


     //"end"可以直接从接口配置模式退出到特权模式
     Router(config)# fa0/0  //进入接口配置模式
     Router(config-if)# end //接口配置模式
     Router#         //退出到特权模式
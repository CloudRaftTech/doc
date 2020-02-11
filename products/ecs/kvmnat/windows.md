# 5.安装WINDOWS系统

#### 挂载镜像

目前云筏NAT产品提供两个镜像（Win10与WinServer2019），如果需要其他镜像可以购买这个服务（[点击购买服务](https://www.liujason.com/exlinks/240)）一次性支付50元。  
在控制面板中的VPS配置选项中，可以选择启动顺序和挂载磁盘：  
![](https://www.liujason.com/wp-content/uploads/2020-1579629289.png)  
选择先CD再Disk，然后选择自己想要挂载的镜像，然后保存，重启服务器后即可生效。  
![](https://www.liujason.com/wp-content/uploads/2020-1579629290.png)  
记得在控制面板中重启服务器！

#### 连接VNC进行安装

根据上面的VNC连接教程，连上机器的VNC，然后点击窗口上方的ctrl alt del按钮，在机器内软重启，在启动选项中根据提示操作，进入安装界面。  
![](https://www.liujason.com/wp-content/uploads/2020-1579629291.png)  
注意，云筏提供的两个镜像是添加了virtio驱动的，如果要提交工单使用其他镜像的话需要注意是否带有virtio驱动。


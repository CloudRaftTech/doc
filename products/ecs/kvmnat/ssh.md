# 1.SSH连接服务器

#### 获取服务器的基础信息

在控制面板中，查看右侧区域的IP信息，将鼠标移动到内网IP上即可查看到**内网IPv4**和公网IPv6地址。这里我们要记录下内网IPv4的地址，本例中为172.17.200.10。  
![](https://www.liujason.com/wp-content/uploads/2020-1579629283.png)  


如果您的本地网络有IPv6环境，那么只需使用IPv6连接服务器即可。对于本地没有IPv6的人来说，这个NAT服务器还需要一些额外配置才能和普通的IPv4服务器一样使用。

由于进行IPv4端口转发的的公网IP是可能发生变动的，因此以查询为准，本例中是：nat-eu-2.cloudraft.cn

**查询页面**：[https://tools.cloudraft.cn/nat-port.php](https://tools.cloudraft.cn/nat-port.php) 输入自己的内网ip（172.xx.xxx.xxx）即可。

#### 计算端口号

每台机器分配5个端口，端口序号（后面说的B）从1~5分别对应22、80、443、10001、10002。可以根据自己服务器的内网IPv4计算出端口，端口格式：1AAAB，其中1为固定数字，AAA为服务器内网IPv4的第四段（D段）前位补零，B为上述端口序号1~5。例如服务器内网IPv4为172.17.200.2，则AAA为002，22号端口映射的公网端口为10021，80端口为10022，以此类推。  
  
本例中因为是172.17.200.10，所以端口号是10101~10105; SSH端口为10101。

#### 测试连接

```text
CloudRaft-Demo:~ cloudraft$ ssh root@nat–eu–2.cloudraft.cn –p 10101
The authenticity of host \\\’[nat–eu–2.cloudraft.cn]:10101 ([88.99.48.50]:10101)\\\’ can\\\’t be established.
ECDSA key fingerprint is SHA256:tvIf426QM1bWb8yv0KeoejpUWUl8PEYw2Q4qUu6fuk4.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added \\\’[virt–nat–eu–1.cloudraft.cn]:10101\\\’ (ECDSA) to the list of known hosts.
Last login: Fri Jan 17 04:39:54 2020 from xxxxxxx
[root@ecs–z3H ~]#
```

如果可以连接，就可以进行下一步的工作了。

#### 若连接失败

这是由于公用IPv4被阻断造成的，请使用FinalShell内置的【海外服务器加速】功能。

Windows版下载地址:  
[http://www.hostbuf.com/downloads/finalshell\_install.exe](http://www.hostbuf.com/downloads/finalshell_install.exe)  
  
macOS版下载地址:  
[http://www.hostbuf.com/downloads/finalshell\_install.pkg](http://www.hostbuf.com/downloads/finalshell_install.pkg)


# 3.宝塔的安装

首先先确保自己能连上SSH，参考前文。为了确保安装成功，请在/etc/hosts中添加如下记录：

```text
45.32.116.160 download.bt.cn
```

#### 一键脚本

使用官方的一键脚本没有任何问题：

```text
yum install –y wget && wget –O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh
```

按y继续：

```text
———————————————————————-
| Bt–WebPanel 7.0 FOR CentOS/Ubuntu/Debian
———————————————————————-
| Copyright © 2015–2099 BT–SOFT(http://www.bt.cn) All rights reserved.
———————————————————————-
| The WebPanel URL will be http://SERVER_IP:8888 when installed.
———————————————————————-

Do you want to install Bt–Panel to the /www directory now?(y/n):
```

然后脚本全自动运行安装宝塔，全程大约1~5分钟，本例为2分钟。

```text
Complete!
success
Stopping Bt–Tasks… done
Stopping Bt–Panel… done
Starting Bt–Panel… done
Starting Bt–Tasks… done
==================================================================
Congratulations! Installed successfully!
==================================================================
Bt–Panel: http://[2a01:4f8:b16:1051::52:7586]:8888/57bd0bdf
username: y4otwn2w
password: 4f6d2d6d
Warning:
If you cannot access the panel,
release the following port (8888|888|80|443|20|21) in the security group
==================================================================
Time consumed: 2 Minute!
```

#### 获取宝塔的登录信息

IPv6地址（直接可以访问）：http://\[2a01:4f8:b16:1051::52:7586\]:8888/57bd0bdf  
IPv4地址（需根据下面的操作设置）：http://nat-eu-2.cloudraft.cn:10104/57bd0bdf  
username: y4otwn2w  
password: 4f6d2d6d

#### 修改宝塔IPv4访问端口

安装完成后执行bt，键入8，将宝塔监听的端口修改为10001。根据之前的端口计算方式，可以知道本例中的10001端口被映射为公网IP的10104端口，因此访问方式为：http://nat-eu-2.cloudraft.cn:10104/  
注意！修改完监听端口后，IPv6的端口也会变为10001


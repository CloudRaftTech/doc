# 4.CloudFlare建站及转发IPv4+v6端口

#### 注册CloudFlare

首先需要注册CloudFlare账户：[https://www.cloudflare.com ](https://www.cloudflare.com)

如果有需要可以使用云筏提供的免费CloudFlarePartner：[https://cf.cloudraft.cn](https://cf.cloudraft.cn) 以及30元/年的CloudFlare Pro订阅：[https://www.cloudraft.cn/cart.php?gid=19](https://www.cloudraft.cn/cart.php?gid=19)

#### 宝塔设置监听IPv6

面板设置监听IPv6即可：  
![](https://www.liujason.com/wp-content/uploads/2020-1579629286.png)

#### CloudFlare设置IPv6解析

![](https://www.liujason.com/wp-content/uploads/2020-1579629287.png)  
等DNS生效了就好了，测试地址：[https://cloudraft-nat-test.liujason.com/](https://www.liujason.com/exlinks/241)  
![](https://www.liujason.com/wp-content/uploads/2020-1579629288.png)

### 进阶用法

CloudFlare实际上不仅支持常规的80和443端口，同时还支持了以下端口，因此也可以通过CloudFlare来转发这些端口实现IPv6-&gt;IPv4+v6的访问，让小鸡的玩法多样起来！

```text
HTTP ports supported by Cloudflare:
80
8080
8880
2052
2082
2086
2095
HTTPS ports supported by Cloudflare:
443
2053
2083
2087
2096
8443
```

这些端口都是可以被CloudFlare转发的，具体玩法请参考本章的【高阶玩法】内容。另外欢迎加入QQ群互相讨论

* [官方QQ群](https://jq.qq.com/?_wv=1027&k=5G3Fzrs): 519447973

。


# 无法解析域名\|Name or service not known

#### Q：服务器无法解析域名、Name or service not known

A：由于上游服务器供应商Hetzner的安全警告，我们阻断了IPv4 NAT接口的出网方向UDP协议，防止用户对外进行UDP攻击。解决方案：将DNS设置为IPv6DNS，如google的2001:4860:4860::8888 具体方法如下：

CentOS、Debian、Ubuntu等：

```text
vi /etc/resolv.conf
#将nameserver改为2001:4860:4860::8888和2001:4860:4860::8844
```

Windows：

依次打开【控制面板】&gt;【网络和Internet项】&gt;【查看网络状态和任务】&gt;【更改适配器设置】，查看到默认网卡，右键点击网卡，选择【属性】，找到【Internet协议4（TCP/IPV4）】双击后，即可在下图中编辑DNS，改为2001:4860:4860::8888和2001:4860:4860::8844。

![](../../../../.gitbook/assets/image%20%282%29.png)




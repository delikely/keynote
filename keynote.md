# 欺骗攻击与防御
# 欺骗攻击与防御


## 1. hosts


- 影响范围：单机

<font color=red >在哪里影响?</font> 

> 
* Windows系统hosts位于 C:\Windows\System32\drivers\etc\hosts
* Android（安卓）系统hosts位于 /system/etc/hosts
* Mac（苹果电脑）系统hosts跟Linux一样位于 /etc/hosts
* iPhone（iOS）系统hosts跟Linux Mac一样位于 /etc/hosts
* Linux系统hosts位于 /etc/hosts

</br>
<font color=red >用什么影响?</font> 
* 老D：https://laod.org/hosts/2016-google-hosts.html

</br>
<font color=red >怎么操作?</font> 
</br>
* 修改hosts后生效的方法：

Windows
开始 -> 运行 -> 输入cmd -> 在CMD窗口输入
> ipconfig /flushdns

Linux
终端输入
> sudo rcnscd restart
对于systemd发行版，请使用命令
> sudo systemctl restart NetworkManager

Mac OS X终端输入
> sudo killall -HUP mDNSResponder

Android
> 开启飞行模式 -> 关闭飞行模式

通用方法
> 拔网线(断网) -> 插网线(重新连接网络)

</br>

## 2. dns服务器
 
DNSmasq是一个小巧且方便地用于配置DNS和DHCP的工具，适用于小型网络，它提供了DNS功能和可选择的DHCP功能。

主配置文件/etc/dnsmasq.conf 

```
/etc/init.d/dnsmasq start   #开启服务
/etc/init.d/dnsmasq restart #重启服务

```


## 3. 钓鱼网站

钓鱼网站通常指伪装成银行及电子商务，窃取用户提交的银行帐号、密码等私密信息的网站，可用电脑管家进行查杀。“钓鱼”是一种网络欺诈行为，指不法分子利用各种手段，仿冒真实网站的URL地址以及页面内容，或利用真实网站服务器程序上的漏洞在站点的某些网页中插入危险的HTML代码，以此来骗取用户银行或信用卡账号、密码等私人资料。

域名相似的钓鱼网站==野鸡大学 


## 4. captive portal 技术
captive portal，就是强制主页。校园网里面的验证通常都是通过一个网页验证来完成，不管你点要访问哪一个网站，它都会强制给你转到我们设置的主页。

其实这个技术主要的还是用在authentication。

 **无线热点认证解决方案:wifidog **

![wifidog](http://dev.wifidog.org/chrome/site/wifidog.png)

现在许多做收费Wi-Fi接入的都是用wifidog。

## 5.openwrt （系统平台支持）
![OpenWrt](https://dev.openwrt.org/chrome/site/openwrt-logo.png)

OpenWrt 可以被描述为一个嵌入式的 Linux 发行版，（主流路由器固件有 dd-wrt,tomato,openwrt三类）而不是试图建立一个单一的、静态的系统。OpenWrt的包管理提供了一个完全可写的文件系统，从应用程序供应商提供的选择和配置，并允许您自定义的设备，以适应任何应用程序。

当Linksys释放 WRT54G/GS 的源码后。当Linksys释放 WRT54G/GS 的源码后，网上出现了很多不同版本的 Firmware 去增强原有的功能。大多数的 Firmware 都是99%使用 Linksys的源码，只有1%是加上去的，每一种 Firmware 都是针对特定的市场而设计，这样做有2个缺点，第一个是难以集合各版本Firmware的长处，第二个是这版本距离 Linux 正式发行版越来越远。

OpenWrt 选择了另一条路，它从零开始，一点一点的把各软件加入进去，使其接近 Linksys 版 Firmware的功能，而OpenWrt 的成功之处是它的文件系统是可写的，开发者无需在每一次修改后重新编译，令它更像一个小型的 Linux 电脑系统。


附：Markdown 图床 Github




























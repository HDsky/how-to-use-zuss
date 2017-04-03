# how to use zuss {#how-to-use-zuss}

本文参考了[https://www.zhaoj.in/read-3736.html](https://www.zhaoj.in/read-3736.html)

1. 面板里的配置

注册登录啥的自行领会，谢谢。

进入主页后点击右边的资料编辑

向下拉到SSR协议&混淆设置，将协议修改为auth\_sha1\_v4，混淆方式修改为tls1.2\_ticket\_auth

然后我们来看分操作系统的设置

1. Microsoft Windows

首先到[https://github.com/shadowsocksr/shadowsocksr-csharp/releases](https://github.com/shadowsocksr/shadowsocksr-csharp/releases) 下载最新版本的ShadowSocksR

下载完之后，解压，运行，导入节点

首先是解压，然后得到这个目录：

请确保你安装了.NET Framework运行时（对于Windows 8及更新版本的Windows会自带4.0以上版本；对于Windows Vista和Windows 7会自带2.0版本），可以先尝试运行ShadowsocksR-dotnet4.0.exe，如果出现错误再尝试运行ShadowsocksR-dotnet2.0.exe。

如果都错误那就是没有安装（比如说Windows XP），请到微软官网下载安装.NET Framework运行时4.0版本：[https://www.microsoft.com/zh-CN/download/details.aspx?id=17851](https://www.microsoft.com/zh-CN/download/details.aspx?id=17851)

打开以后会弹出一个添加服务器的窗口，先关闭它。

点开面板右侧的节点列表，再点日本1

向下拉直到出现二维码

在系统托盘处找到小飞机图标，点击右键-二维码扫描。弹出窗口后点确定。

更新PAC，可在绕过大陆IP和GFWList之间选择。

绕过大陆IP：所有出国流量不管有没有被墙都走代理

GFWList：只有部分被墙的网站才走代理，这个列表可能更新不及时

开启系统代理为PAC模式

1. Apple iOS

iOS上有三个客户端可以使用，分别是Surge、 Shadowrocket 和 Potatso

 然而两个都是付费的，希望获取免费Shadowrocket账号的请联系群主。

打开Shadowrocket，点击右上角的+号，类型选 ShadowsocksR，依次按照节点说明填入服务器地址、代理端口、密码、加密方式，并且设置混淆和协议，然后点击右上角的Done就配置完了。

![25](export/assets/25.png)

![26](export/assets/26.png)

第一次运行会弹出一个创建VPN的窗口，点击Allow，再输入密码或进行Touch ID认证，然后重新点击连接。

1. Android

首先请下载安装APP [https://github.com/shadowsocksr/shadowsocksr-android/releases](https://github.com/shadowsocksr/shadowsocksr-android/releases)


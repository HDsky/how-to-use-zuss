# How to use zuss

本文为合作编辑，感谢各位合作者的辛勤付出：lyic，imzbb，HDsky

最后编辑日期为：2017/4/3

## 1.面板里的配置

注册登录啥的自行领会，谢谢。

进入主页后点击右边的资料编辑

~~向下拉到SSR协议&混淆设置，将协议修改为auth\_sha1\_v4，混淆方式修改为tls1.2\_ticket\_auth（可以不做这些改动）~~

![](/assets/chaos.png)

## 2.然后我们来看操作系统的设置

### 1.Windows客户端

首先到[这里下载](https://github.com/shadowsocksr/shadowsocksr-csharp/releases) 下载最新版本的ShadowSocksR

#### 1.1首先是解压

然后得到这个目录：

![](/assets/unzip.png)

请确保你安装了.NET Framework运行时（对于Windows 8及更新版本的Windows会自带4.0以上版本；对于Windows Vista和Windows 7会自带2.0版本），可以先尝试运行ShadowsocksR-dotnet4.0.exe，如果出现错误再尝试运行ShadowsocksR-dotnet2.0.exe。

如果都错误那就是没有安装（比如说Windows XP），请到微软官网下载安装.NET Framework运行时4.0版本：[点击下载](https://www.microsoft.com/zh-CN/download/details.aspx?id=17851)

#### 1.2添加节点

打开以后会弹出一个添加服务器的窗口，先关闭它。

点开面板右侧的节点列表，再点你想要建立连接的节点![](/assets/table0.png)![](/assets/table1.png)

![](/assets/table2.png)![](/assets/table3.png)

向下拉直到出现二维码，保持网页的开启状态

在系统托盘处找到小飞机图标，点击右键-二维码扫描。弹出窗口后点确定。

![](/assets/fly.png)

![](/assets/erweima.png)

然后继续右键选择-服务器-选择你刚刚添加的节点

![](/assets/server.png)

#### 1.3模式的选择

主要能选择的模式有两种，一种是全局模式，另一种则是PAC模式，在这里我们推荐使用PAC模式。（值得注意的是，Shadowsocks仅能作为网页代理使用，在一些软件中使用需配合软件自带的代理设置或配合socks代理转http的软件，在此不做描述）

全局模式：全局模式就是你是用浏览器访问的所有网站都通过代理来访问。  
而PAC模式则是通过调整PAC文件来控制哪些网站走代理，哪些网站不通过代理访问。  
**下面介绍两个个PAC文件：**

绕过大陆IP：所有出国流量不管有没有被墙都走代理；

GFWList：只有部分被墙的网站才走代理，这个列表可能更新不及时；

根据自己的需求选择不同的PAC文件并更新。

然后开启系统代理为PAC模式

![](/assets/changePAC.png)

### 2.Apple iOS

iOS上推荐这四个客户端使用，分别是Surge、Shadowrocket 和 Potatso以及Wingy

下载地址如下

Surge：[点此下载](https://itunes.apple.com/cn/app/surge-web-developer-tool-and-proxy-utility/id1040100637?mt=8)

Shadowrocket：[点此下载](https://itunes.apple.com/cn/app/shadowrocket/id932747118?mt=8)

Potatso：[点此下载](https://itunes.apple.com/cn/app/%E5%9C%9F%E8%B1%86%E4%B8%9D-potatso-%E5%BC%BA%E5%A4%A7%E7%9A%84%E7%BD%91%E7%BB%9C%E5%B7%A5%E5%85%B7/id1070901416?mt=8)

Wingy：[点此下载](https://itunes.apple.com/cn/app/shadowsocks-wingy-proxy-for-http-socks5-ss/id1148026741?mt=8)

下面以Shadowrocket为例，介绍下ios端的使用。

打开Shadowrocket，点击右上角的+号，类型选 ShadowsocksR，依次按照节点说明填入服务器地址、代理端口、密码、加密方式，并且设置混淆和协议，然后点击右上角的Done就配置完了。

![](/assets/Shadowrocketios.png)

第一次运行会弹出一个创建VPN的窗口，点击Allow，再输入密码或进行Touch ID认证，然后重新点击连接。

### 3.Android

首先请下载安装APP [点此下载](https://github.com/shadowsocksr/shadowsocksr-android/releases)

配置过程与IOS客户端类似。


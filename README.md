# How to use zuss

本文为合作编辑，感谢各位合作者的辛勤付出：lyic，imzbb，HDsky

最后编辑日期为：2019/01/15

Gitbook连接：[https://hdsky.gitbooks.io/how-to-use-zuss/content/](https://hdsky.gitbooks.io/how-to-use-zuss/content/)
>注意：因为ShadowSocksR的开发者已经宣布停止继续开发该项目并删除了之前的仓库，下面提供的下载链接是他人备份的仓库，当然如果你更喜欢原版ShadowSocks的话也是可以的。建议寻求[可信赖的下载渠道](http://shadowsocks.org/en/download/clients.html)，并在下载后进行校验。

## 面板

由于面板可视化界面已经非常清晰明了，在此不做过多赘述。作此教程对大家在多平台客户端的设置做个指引。
如果有什么不明白的请询问身边的朋友，不对**不善于学习的人**回答任何问题。

尽管在各系统版本安装调试完成后已经能够正常工作，但还是建议各位在PC上能按照浏览器插件设置一章进行后续的操作，此举将使今后的使用更加便捷。

## 客户端设置

* [Windows](#windows)
* [iOS](#apple-ios)
* [Android](#android)
* [Linux](#linux)
* [Mac](#mac)
* [浏览器插件设置](#Chrome&Firefox)

### Windows

#### 下载

下载链接已移除 可以选择从此处寻找你需要的客户端 https://github.com/shadowsocks

#### 解压

将其解压到你指定的文件夹中保存好，会得到这个目录：

![![](/assets/unzip.png)](/assets/SSR.png)

确保你安装了 .NET Framework

* Windows 8 及更新版本的 Windows 会自带 4.0 或更新版本；
* 对于 Windows Vista 和 Windows 7 则会自带2.0版本，请到微软官网[下载安装 .NET Framework 运行库 4.0 版](https://www.microsoft.com/zh-CN/download/details.aspx?id=17851)。

#### 添加节点

打开以后会弹出一个添加服务器的窗口，先关闭它。

看到**面板**下方的“连接信息 以及 All-in-One(快速配置指导)”，点击 SHADOWSOCKSR -> WINDOWS，看到 SSR 订阅地址，复制“普通端口地址”后面的链接，暂时不要理会“单端口多用户端口地址”链接。

![](/assets/SSR_book.png)

在系统托盘处找到小飞机图标，单击右键进入菜单，选择服务器 -> SSR服务器订阅设置，将订阅地址设置为普通端口地址，其他参数留空，确定之后再点击“更新 SSR 服务器订阅（不通过代理）”。

![](/assets/SSR_02.png)

然后继续右键 -> 服务器 -> 选择一个刚刚通过订阅添加的节点

![](/assets/SSR_03.png)

#### 系统代理模式的选择

主要能选择的系统代理模式有两种，一种是**全局模式**，另一种则是**PAC模式**，在这里我们推荐使用PAC模式。

>值得注意的是，ShadowsocksR仅设置了系统默认代理，在一些不读取使用系统默认代理设置的软件中使用需配合软件自带的代理设置或配合SOCKS5代理转http的软件，在此略过不表。

* 全局模式：用浏览器（或其他支持系统代理的应用）访问的所有网站都通过SSR软件来访问。  
* PAC模式：系统代理设置为PAC。通过PAC文件来控制哪些网站走代理，哪些网站不通过代理访问。  

**默认的两个PAC配置：**

* 绕过大陆IP：判断IP地址国别，所有出国流量不管有没有被墙都走代理；

* GFWList：只有部分被墙的网站才走代理，这个列表由志愿者贡献，可能不包含所有被墙的网站。

根据自己的需求选择不同的PAC文件并更新，建议新用户可采用GFWList这个PAC配置。

然后开启系统代理为PAC模式

![](/assets/changePAC.png)

``可选：按照[浏览器插件设置]对Chrome或Firefox进行插件的安装设置。``

Enjoy the free Internet.

### Apple iOS

对于非越狱设备，部分代理软件需要使用 Apple 在 iOS 9 中引入的新框架 Network Extension，请确保您设备的 iOS 版本足够支持客户端运行。
我们推荐五个客户端，分别是[Surge](https://itunes.apple.com/us/app/surge-3-web-developer-tool/id1329879957?mt=8)、[Shadowrocket](https://appsto.re/us/UDjM3.i)、[Potatso](https://itunes.apple.com/us/app/potatso-2/id1162704202?mt=8)、[Wingy（付费版）](https://itunes.apple.com/us/app/wingy-shadow-vpn-for-http-socks5-ss/id1148026741?mt=8)、[Wingy（免费版）](https://itunes.apple.com/us/app/wingy-http-s-socks5-proxy-utility/id1178584911?mt=8)、[Potatso Lite](https://itunes.apple.com/us/app/potatso-lite/id1239860606?mt=8)。
>因受中国相关政策及作者个人意愿等影响，这五款软件已下架中国区 App Store，如您在中国区已购上述下架软件，那么需要更换您的 Apple ID 区域才能重新下载，请参考[此处](http://www.mk52.cn/jiaocheng/2053.html)，对换区造成的其他后果自负，望周知。（在此十分建议各位拥有一个非中国区 Apple ID 并使用喜欢的形式购买 Shadowrocket，它绝对会让你喜欢。
>同时，因早前中国区应用商店政策变更，不对其他目前还在中国区上架的代理软件进行推荐。

可以通过**二维码扫描**的方式添加节点，代理软件中带有的二维码扫描功能，扫描面板里节点列表中的二维码即可完成对节点的添加工作。（注意：二维码有两种，一种是ShadowSocks格式，另一种是ShadowSocksR格式，请根据代理软件对与这两种方式的支持情况酌情选择）

第一次运行时会弹出一个创建VPN的窗口，点击“允许/Allow“，再输入密码或进行Touch ID/Face ID认证，然后完成连接。

Enjoy the free Internet.

### Android

首先[下载安装APP](https://github.com/shadowsocks)。


配置过程与iOS客户端类似，推荐使用二维码扫描的方式添加节点。

Enjoy the free Internet.

### Linux

#### 1. 下载安装shadowsocks 客户端

python版
```shell
pip install shadowsocks
```
C语言版
```shell
apt-get install shadowsocks-libev
```
又或者通过[此篇教程](https://github.com/shadowsocks/shadowsocks-qt5/wiki/Installation)安装Qt版本的shadowsocks

#### 2. 设置系统代理

在设置完成后还需要对Ubuntu系统进行设置，打开Ubuntu的设置-网络-代理设置，将Socks的代理地址参数设置为127.0.0.1 端口号设置为1080（默认参数，如果你自定义了参数，请根据实际情况进行填写）

完成了上面的设置后，浏览网页的全部数据都是使用的代理模式，所以还没达到完美。需要在浏览器中安装一个插件Proxy SwitchyOmega对代理进行分流管理。

#### Chrome&Firefox

* 如果你用 **Chrome**：访问 [Chrome 应用商店安装 SwitchyOmega](https://chrome.google.com/webstore/detail/proxy-switchyomega/padekgcemlokbadohgkifijomclgjgif)。
* 如果你用 **Mozilla Firefox**：访问 [Mozilla Add-Ons 安装 SwitchyOmega](https://addons.mozilla.org/en-US/firefox/addon/switchyomega/)。

如果你无法访问上述提供的地址并完成安装，请从插件官网获取安装包或者其他帮助 https://switchyomega.com/

安装好后进入插件的设置界面在Proxy情景模式下按照如下图所示填写：
![](/assets/proxy.png)

然后在Auto Switch情景模式下如下图填写：
![](/assets/Autoproxy.png)

* 填入的地址为 https://raw.githubusercontent.com/gfwlist/gfwlist/master/gfwlist.txt

在浏览器右上角点击插件按钮，然后选择自动切换规则模式，这样只要在规则列表里面的网站都会翻墻访问。

对于没在翻墻规则里面的网站，可以自己添加规则（但资源无法加载时，插件图标会有提示，点击后就可以看到快速添加方法）

![](/assets/switch.png)

#### 3. 还原系统代理设置
**打开Ubuntu的设置-网络-代理设置，将设置更改为不使用代理。**

Enjoy the free Internet.

### Mac

可以使用[ShadowsocksX\-NG](https://github.com/shadowsocks/ShadowsocksX-NG)，配置方式与 window 版类似。

``可选：按照"浏览器插件设置"对Chrome或Firefox进行插件的安装设置。``

## One More Thing

由于Shadowsocks是Socks代理，在Windows系统当中不能用于命令行以及应用内代理（软件支持Socks除外），需要使用其他软件将Socks代理转为Http代理，在这里推荐使用``Proxifier``作为将Socks转为类似于VPN的全局代理的软件。

另外对于Linux&Mac用户在使用一些命令行工具的时候会遇到国外网站无法访问或者速度慢的情况，这时候可以使用``Proxychains-NG``对Terminal中执行的命令进行代理。具体使用信息可以参考作者的Github项目主页。

## 参考文献

[1]小灰木头兔. Chrome+SwitchyOmega+Shadowsocks 图文教程完整篇[EB/OL]. http://wxhp.org/shadowsocksr.html.

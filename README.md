# How to use zuss

本文为合作编辑，感谢各位合作者的辛勤付出：lyic，imzbb，HDsky

最后编辑日期为：2017/12/15

Gitbook连接：[https://hdsky.gitbooks.io/how-to-use-zuss/content/](https://hdsky.gitbooks.io/how-to-use-zuss/content/)
>注意：因为ShadowSocksR的开发者已经宣布停止继续开发该项目并删除了之前的仓库，下面提供的下载链接是他人备份的仓库，当然如果你更喜欢原版ShadowSocks的话也是可以的。建议寻求[可信赖的下载渠道](http://shadowsocks.org/en/download/clients.html)，并在下载后进行校验。

## 面板

由于面板可视化界面已经非常清晰明了，在此不做过多赘述。作此教程对大家在多平台客户端的设置做个指引。
如果有什么不明白的请询问身边的朋友，不对**不善于学习的人**回答任何问题。
在此注意的是注册时默认使用的是ShadowSocksR的混淆设置，只能使用ShadowSocksR的客户端，如需要使用ShadowSocks的客户端，则需要在面板中对混淆以及协议或者加密方式进行修改，望周知

## 客户端设置

* [Windows](#windows) 
* [Apple iOS](#apple-ios)
* [Android](#android)
* [Linux](#linux)
* [Mac](#mac)

### Windows

#### 下载

[下载 ShadowSocksR (with HDsky Mod)](https://github.com/HDsky/gfwlist/raw/master/ssr-win-by-hdsky.7z) 

#### 解压

得到这个目录：

![![](/assets/unzip.png)](/assets/SSR.png)

请确保你安装了.NET Framework

* Windows 8及更新版本的Windows会自带4.0或更新版本；
* 对于Windows Vista和Windows 7会自带2.0版本。  

可以先尝试运行ShadowsocksR.exe

如果出现运行错误那就请到微软官网[下载安装 .NET Framework 运行库 4.0 版](https://www.microsoft.com/zh-CN/download/details.aspx?id=17851)。之后启动ShadowsocksR.exe。

#### 添加节点

打开以后会弹出一个添加服务器的窗口，先关闭它。

看到**面板**下方的“连接信息 以及 All-in-One(快速配置指导)”，点击 SHADOWSOCKSR	 -> WINDOWS，看到 SSR 订阅地址，复制“普通端口地址”后面的链接，暂时不要理会“单端口多用户端口地址”链接。

![](/assets/SSR_book.png)

在系统托盘处找到小飞机图标，单击右键进入菜单，选择服务器—>SSR服务器订阅设置，将订阅地址设置为普通端口地址，其他参数留空，确定之后再更新 SSR 服务器订阅（不通过代理）。

![](/assets/SSR_02.png)

然后继续右键选择-服务器-选择一个刚刚通过订阅添加的节点

![](/assets/SSR_03.png)

#### 系统代理模式的选择

主要能选择的系统代理模式有两种，一种是**全局模式**，另一种则是**PAC模式**，在这里我们推荐使用PAC模式。

>值得注意的是，ShadowsocksR仅设置了系统默认代理，在一些不读取使用系统默认代理设置的软件中使用需配合软件自带的代理设置或配合SOCKS5代理转http的软件，在此略过不表。

* 全局模式：全局模式就是你是用浏览器（或其他支持系统代理的应用）访问的所有网站都通过SSR软件来访问。  
* PAC模式：系统代理设置为PAC。通过PAC文件来控制哪些网站走代理，哪些网站不通过代理访问。  

**两个PAC文件：**

* 绕过大陆IP：判断IP地址国别，所有出国流量不管有没有被墙都走代理；

* GFWList：只有部分被墙的网站才走代理，但这个列表可能更新不及时；

根据自己的需求选择不同的PAC文件并更新，在此建议新用户可采用使用GFWList的PAC模式。

然后开启系统代理为PAC模式

![](/assets/changePAC.png)

### Apple iOS

对于非越狱设备，VPN 软件需要使用 Apple 在 iOS 9 中引入的新框架 Network Extension，请确保您设备的 iOS 版本足够支持客户端运行。
我们推荐五个客户端，分别是[Surge](https://itunes.apple.com/us/app/surge-web-developer-tool-and-proxy-utility/id1040100637?mt=8)、[Shadowrocket](https://appsto.re/us/UDjM3.i)、[Potatso](https://itunes.apple.com/us/app/potatso-2/id1162704202?mt=8)、[Wingy（付费版）](https://itunes.apple.com/us/app/wingy-shadow-vpn-for-http-socks5-ss/id1148026741?mt=8)、[Wingy（免费版）](https://itunes.apple.com/us/app/wingy-http-s-socks5-proxy-utility/id1178584911?mt=8)、[Potatso Lite](https://itunes.apple.com/us/app/potatso-lite/id1239860606?mt=8)。
>因受中国相关政策及作者个人意愿等影响，这五款软件已下架中国区 App Store，如您在中国区已购上述下架软件，那么需要更换您的 Apple ID 区域才能重新下载，请参考[此处](http://www.mk52.cn/jiaocheng/2053.html)，对换区造成的其他后果自负，望周知。（在此十分建议各位拥有一个非中国区 Apple ID 并使用喜欢的形式购买 Shadowrocket，它绝对会让你喜欢。
在此之外，不对任何目前还在国区的代理软件进行推荐。1）我没用过；2）我只使用过上面的五款软件；
可以使用**二维码扫描**的方式添加节点，通过代理软件中带有的二维码扫描功能，扫描面板里节点列表中的二维码即可完成对节点的添加工作。（注意：二维码有两种，一种是ShadowSocks一种是ShadowSocksR请根据代理软件对与这两种方式的支持情况酌情选择。）

第一次运行会弹出一个创建VPN的窗口，点击允许/Allow，再输入密码或进行Touch ID/Face ID认证，然后重新点击连接。

### Android

首先[下载安装APP](https://github.com/esdeathlove/panel-download/blob/master/ssr-android.apk?raw=true)。

配置过程与iOS客户端类似，也推荐用二维码扫描的方式添加节点。

### Linux

推荐使用[Python client](https://github.com/ssrbackup/shadowsocksr)。以Ubuntu 16.04为例

#### 1. 下载 shadowsocksr-python

```shell
sudo apt install git
git clone https://github.com/ssrbackup/shadowsocksr.git
```
或者

```shell
wget https://github.com/ssrbackup/shadowsocksr/archive/manyuser.zip
```

#### 2. 进入刚下载的目录中的shadowsocks文件夹

```shell
cd shadowsocksr-manyuser/shadowsocks
```
#### 3. 运行

参数说明：-p 端口 -k 密码  -m 加密方式 -O 协议 -o 混淆
```shell
python local.py -s server_ip -p 443 -k password -m aes-256-cfb -o http_simple
```

如果要后台运行：
```shell
python local.py -s server_ip -p 443 -k password -m aes-256-cfb -d start
```
如果要停止/重启：
```shell
python local.py -d stop/restart
```
查看日志：
```shell
tail -f /var/log/shadowsocks.log
```
#### 4. 进阶

可以通过建立 JSON 文件的方式来实现代理的开启。
在面板中已经有写好的 JSON 文件可以直接拷贝下来，现在当前目录建立一个文件。

```shell
vi ssr.json
```
或者使用对新手更友好的nano编辑器

```shell
nano ssr.json
```

然后把拷贝好的内容粘贴进去。使用下面的命令就能运行了（其中<PATH>为你放置文件的目录）

```shell
python local.py -c <PATH>/ssr.json
```
后台运行：
```shell
python local.py -c <PATH>/ssr.json -d start
```
如果要停止/重启：
```shell
python local.py -d stop/restart
```
#### 5. 设置系统代理

在设置完成后还需要对Ubuntu系统进行设置，打开Ubuntu的设置-网络-代理设置，将Socks的地方设置为127.0.0.1 端口号设置为1080

#### 6. 对浏览器设置分流

完成了上面的设置后，浏览网页是全部进入代理模式的，所以还没达到完美。
需要在浏览器中安装一个插件Proxy SwitchyOmega。

* 如果你用 **Chrome**：访问 [Chrome 应用商店安装 SwitchyOmega](https://chrome.google.com/webstore/detail/proxy-switchyomega/padekgcemlokbadohgkifijomclgjgif)。
* 如果你用 **Mozilla Firefox**：访问 [Mozilla Add-Ons 安装 SwitchyOmega](https://addons.mozilla.org/en-US/firefox/addon/switchyomega/)。

安装好后点击左侧的新增情景模式，我们先新增一个 SS 代理。

![](/assets/SwitchyOmega1.png)

像这样设置

![](/assets/SwitchyOmega2.png)

然后新增一个切换模式

![](/assets/SwitchyOmega3.png)


像这样设置
* 填入的地址为https://raw.githubusercontent.com/gfwlist/gfwlist/master/gfwlist.txt

![](/assets/SwitchyOmega4.png)

在浏览器右上角点击插件按钮，然后选择自动切换规则模式，这样只要在规则列表里面的网站都会翻墻访问。

对于没在翻墻规则里面的网站，可以自己添加规则（但资源无法加载时，插件图标会有提示，点击后就可以看到快速添加方法）

#### 还原系统代理设置
**打开Ubuntu的设置-网络-代理设置，将设置更改为不使用代理。**

教程参考了下面的链接 http://wxhp.org/shadowsocksr.html


### Mac

未完待续

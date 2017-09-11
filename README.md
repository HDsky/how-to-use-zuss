# How to use zuss

本文为合作编辑，感谢各位合作者的辛勤付出：lyic，imzbb，HDsky

最后编辑日期为：2017/9/11

Gitbook连接：[https://hdsky.gitbooks.io/how-to-use-zuss/content/](https://hdsky.gitbooks.io/how-to-use-zuss/content/)
>注意：因为ShadowSocksR的开发者已经宣布停止继续开发该项目并删除了之前的仓库，下面提供的下载链接是他人备份的仓库，当然如果你喜欢原版的ShadowSocks的话也是是可以使用原版的ShadowSocks，建议寻求可信赖的下载取道，在下载后进行校验。

## 面板

由于面板可视化界面已经非常清晰明了，在此不做过多赘述。  
作此教程对大家在客户端的设置做个指引。

## 客户端设置

* [Windows](#windows) 
* [Apple iOS](#apple-ios)
* [Android](#android)
* [Linux](#linux)

### Windows

#### 下载

[下载最新版本的ShadowSocksR](https://github.com/ssrbackup/shadowsocks-rss) 

#### 解压

得到这个目录：

![](/assets/unzip.png)

请确保你安装了.NET Framework
  
* Windows 8及更新版本的Windows会自带4.0以上版本；
* 对于Windows Vista和Windows 7会自带2.0版本。  

可以先尝试运行ShadowsocksR-dotnet**4.0**.exe，如果出现错误再尝试运行ShadowsocksR-dotnet**2.0**.exe。

如果都错误那就请到微软官网[下载安装.NET Framework运行时4.0版本](https://www.microsoft.com/zh-CN/download/details.aspx?id=17851)

#### 添加节点

打开以后会弹出一个添加服务器的窗口，先关闭它。

点开**面板**右侧的节点列表，再点你想要建立连接的节点

![](/assets/table0.png)
![](/assets/table1.png)
![](/assets/table2.png)
![](/assets/table3.png)

向下拉直到出现二维码，保持网页的开启状态

在系统托盘处找到小飞机图标，点击右键-二维码扫描。弹出窗口后点确定。

![](/assets/fly.png)
![](/assets/erweima.png)

然后继续右键选择-服务器-选择你刚刚添加的节点

![](/assets/server.png)

#### 模式的选择

主要能选择的模式有两种，一种是**全局模式**，另一种则是**PAC模式**，在这里我们推荐使用PAC模式。（值得注意的是，Shadowsocks仅能作为网页代理使用，在一些软件中使用需配合软件自带的代理设置或配合socks代理转http的软件，在此不做描述）

* 全局模式：全局模式就是你是用浏览器访问的所有网站都通过代理来访问。  
* PAC模式：通过调整PAC文件来控制哪些网站走代理，哪些网站不通过代理访问。  

**两个PAC文件：**

* 绕过大陆IP：所有出国流量不管有没有被墙都走代理；

* GFWList：只有部分被墙的网站才走代理，这个列表可能更新不及时；

根据自己的需求选择不同的PAC文件并更新，在此建议新用户可以采用GFWList的PAC模式。

然后开启系统代理为PAC模式

![](/assets/changePAC.png)

### Apple iOS

iOS上推荐这五个客户端使用，分别是
[Surge](https://itunes.apple.com/us/app/surge-web-developer-tool-and-proxy-utility/id1040100637?mt=8)、
[Shadowrocket](https://appsto.re/us/UDjM3.i)和
[Potatso](https://itunes.apple.com/cn/app/土豆丝-potatso-强大的网络工具/id1070901416?mt=8)以及
Wingy：[（付费版）](https://itunes.apple.com/cn/app/shadowsocks-wingy-proxy-for-http-socks5-ss/id1148026741?mt=8)[（免费版）](https://itunes.apple.com/cn/app/wingy-http-s-socks5-proxy-utility/id1178584911?mt=8)、
[Potatso Lite](https://itunes.apple.com/cn/app/potatso-lite-%E5%9C%9F%E8%B1%86%E4%B8%9D%E5%85%A5%E9%97%A8%E7%89%88/id1239860606?mt=8)
>其中因为受中国相关政策的影响，苹果公司已对前四个软件在中国区进行了下架处理，即在中国区仅能下载到Potatso Lite这一款应用，如需要换区请参考[此处链接](http://www.mk52.cn/jiaocheng/2053.html)，对换区造成的其他后果自负，望周知。

推荐使用**二维码扫描**的方式添加节点，[参考windows客户端即可](#添加节点)。

第一次运行会弹出一个创建VPN的窗口，点击Allow，再输入密码或进行Touch ID认证，然后重新点击连接。

### Android

首先[下载安装APP](https://github.com/ssrbackup/shadowsocks-rss)。

配置过程与IOS客户端类似，也推荐用二维码扫描的方式添加节点。

### Linux

推荐使用[Python client](https://github.com/ssrbackup/shadowsocksr)。
以下以Ubuntu16.04为例

1.先安装git并下载shadowsocksr-python
```
sudo apt install git
git clone https://github.com/ssrbackup/shadowsocksr.git
```
2.进入刚下载的目录中的shadowsocks文件夹
```
cd shadowsocksr-manyuser/shadowsocks
```
3.运行

参数说明：-p 端口 -k 密码  -m 加密方式 -o 混淆插件
```
python local.py -s server_ip -p 443 -k password -m aes-256-cfb -o http_simple
```

如果要后台运行：
```
python local.py -s server_ip -p 443 -k password -m aes-256-cfb -d start
```
如果要停止/重启：
```
python local.py -d stop/restart
```
查看日志：
```
tail -f /var/log/shadowsocks.log
```
4.进阶
其实可以通过建立json文件的方式来实现代理的开启。
在面板中已经有写好的json文件可以直接拷贝下来，现在当前目录建立一个文件。
```
vi ssr.json
```
然后把拷贝好的内容粘贴进去。使用下面的命令就能运行了（其中<PATH>为你放置文件的目录）
```
python local.py -c <PATH>/ssr.json
```
后台运行：
```
python local.py -c <PATH>/ssr.json -d start
```
如果要停止/重启：
```
python local.py -d stop/restart
```
5.在设置完成后还需要对Ubuntu系统进行设置，打开Ubuntu的设置-网络-代理设置，将Socks的地方设置为127.0.0.1 端口号设置为1080

6.完成了上面的设置后，浏览网页是全部进入代理模式的，所以还没达到完美。
需要在浏览器中安装一个插件Proxy SwitchyOmega，具体的教程请参考下面的链接，在此不做详细描述。(只看Proxy SwitchyOmega设置那一段就可以啦)
http://wxhp.org/shadowsocksr.html
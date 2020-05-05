# Linux配置v2ray详细教程

> 参考资料：https://mahongfei.com/1776.html

v2ray科学上网的话，windows平台我们可以使用clash，v2rayN等软件，mac的话可以使用clashX等，但是对于linux平台，我们的选择比较少了就，今天介绍一款linux上很好用的图形话界面科学上网工具-Qv2ray。

## step1：下载V2ray客户端

这里以最简单的`AppImage`文件为例.

下载链接客户端：

https://github.com/Qv2ray/Qv2ray/releases/download/v1.99.6/Qv2ray-refs.tags.v1.99.6-linux.AppImage

或者打开网站：https://github.com/Qv2ray/Qv2ray/releases/tag/v1.99.6 选择下图文件

![](https://raw.githubusercontent.com/anxiang1836/FigureBed/master/img/20200505052327.png)

> *注意：建议下载1.99.6及以上版本，其它版本可能出现找不到openssl库。*

下载核心文件：

https://github.com/v2ray/v2ray-core/releases/download/v4.22.1/v2ray-linux-64.zip

或者打开网站：https://github.com/v2ray/v2ray-core/releases/ 选择下图文件

![](https://raw.githubusercontent.com/anxiang1836/FigureBed/master/img/20200505052459.png)

进入v2ray下载的根目录，执行以下命令：

```bash
sudo chmod +x ./Qv2ray-refs.tags.v1.99.6-linux.AppImage
sudo ./Qv2ray-refs.tags.v1.99.6-linux.AppImage
```

## step2：设置一个启动应用程序

创建一个app的启动脚本，会增加app的易用性，那么可以进行如下操作：

```bash
sudo vi /usr/share/applications/Qv2ray.desktop
```

这样就可创建一个在程序列表的应用，在下面的配置文件中，主要修改`Name`、`Exec`、`Icon`，其他的照着抄就行了。

其中，`Exec`即为在Terminal中输入的命令；`Terminal`即为是否打开一个终端。

```bash
[Desktop Entry]
Version=1.0
Name=Qv2ray
Exec=bash /opt/v2ray/run.sh
Terminal=true
Icon=/opt/v2ray/icon.png
Type=Application
Categories=Development
```

## step3：配置Qv2ray

在常规设置里面点击->首选项->常规设置，选择可执行文件和根目录，点击ok保存：

![](https://raw.githubusercontent.com/anxiang1836/FigureBed/master/img/20200505053846.png)

进入首选项->入站设置，勾选上设置代理：

![](https://raw.githubusercontent.com/anxiang1836/FigureBed/master/img/20200505054027.png)

最后，在系统的网络的代理设置中，手动配置上与上面v2ray相同的代理端口，如下图：

![](https://raw.githubusercontent.com/anxiang1836/FigureBed/master/img/20200505054317.png)

> 注意，大部分的时候，是可以开着代理进行的，如果遇到pip/conda/apt-get/docker的操作有异常的话，在网络设置中关掉代理就可以了，让其直接走正常的源就OK了


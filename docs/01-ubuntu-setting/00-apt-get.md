# ubuntu切换国内镜像源

> 参考资料：https://blog.csdn.net/TotoroCyx/article/details/79517202

使用apt-get命令安装包时，由于系统自带的下载源速度较慢。若切换为国内源，将显著提升下载速度。下列是设置步骤：

## step1：清华大学镜像源官网

进入清华大学镜像源[官网](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/)，选择自己的系统，复制相应的配置文字：

> 我的是ubuntu18.04，选择你对应的系统版本就好。

![](https://raw.githubusercontent.com/anxiang1836/FigureBed/master/img/20200505045219.png)

```bash
# 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse

# 预发布软件源，不建议启用
# deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
```

## step2：修改配置

apt-get配置文件所在的目录为/etc/apt，故先进入目录，然后对原配置文件进行一份备份：sudo cp sources.list sources.list.bak，以防丢失。

使用vim或gedit工具打开sources.list文件，将原内容删除，替换为上述新的配置内容。

全部的命令如下：

```bash
cd /etc/apt
sudo cp sources.list sources.list.bak
sudo vi sources.list  
```

## step3：更新源使配置生效

```bash
sudo apt-get update
```

使用`sudo apt-get install`命令进行安装，检验效果，会发现速度有了明显提升。
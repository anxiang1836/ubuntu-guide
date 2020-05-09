# Anaconda

> 参考资料：https://blog.csdn.net/lwgkzl/article/details/89329383

## 1. Terminal安装anaconda3

**Step1:**下载
获取anaconda在清华镜像站的网址，然后在服务器端wget 网址就行了。

清华镜像站中anaconda的所有版本的网址：https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/ 

找到自己想要的那个版本，然后右键 -> 复制链接地址。

接下来在服务器端找一个好的目录，wget + 复制好的地址，运行就好。

```bash
wget https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/Anaconda3-5.3.1-Linux-x86_64.sh
```

**Step2:**安装

下载好之后，在下载目录目录中，出现一个Anaconda3-5.3.1-Linux-x86_64.sh这样子的文件，运行它就好,切换到该文件目录运行

```bash
bash Anaconda3-5.3.1-Linux-x86_64.sh
```

然后接下来一步就按照提示来操作就好了。

## 2. 配置zshrc文件

(待补充)
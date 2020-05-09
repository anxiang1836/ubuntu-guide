# 显卡驱动&CUDA

> 参考资料：https://blog.csdn.net/wf19930209/article/details/81877822#NVIDIA_25

##1. nouveau驱动？

nouveau，是一个自由及开放源代码显卡驱动程序，是为Nvidia的显示卡所编写，也可用于属于系统芯片的NVIDIA Tegra系列，此驱动程序是由一群独立的软件工程师所编写，Nvidia的员工也提供了少许帮助。在安装Ubuntu之后，默认就是nouveau驱动的。

> 该项目的目标为利用逆向工程Nvidia的专有Linux驱动程序来创造一个开放源代码的驱动程序。
>
> 所以nouveau开源驱动基本上是不能正常使用的，性能极低，在正常浏览滚动网页的时候也能感觉的出来，会有比较明显的掉帧情况的。

## 2.安装nvidia驱动

> 安装NVIDIA的驱动有若干种方式，比如说：手动禁止nouveau后进行操作，显然，是比较复杂的，而且容易出现其他奇奇怪怪的问题。
>
> 所以这里选择一种比较容易的方式：使用**ubuntu官方源**的形式安装的。

**Step1:**带命令行版本安装工具**ubuntu-drivers**,终端输入:

```bash
ubuntu-drivers devices   # 查询所有ubuntu推荐的驱动
```

**Step2:**安装所有推荐的驱动程序，终端输入:

```bash
sudo ubuntu-drivers autoinstall
```

**Step3:**安装完成后，**重启**就可以了。

## 3.安装CUDA&CuDnn

> 安装cuda：https://blog.csdn.net/wf19930209/article/details/81879514
>
> 解决nvcc找不到的问题：[附上超长链接](https://blog.csdn.net/rtygbwwwerr/article/details/73656876?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromBaidu-1&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromBaidu-1)
>
> 安装cudnn：https://blog.csdn.net/quantum7/article/details/82895001
# 自动挂载硬盘

**Step1：**查看磁盘分区情况：

```
sudo fdisk -l
```

**Step2：**用Ubuntu自带的`磁盘`工具进行分区：

![](https://raw.githubusercontent.com/anxiang1836/FigureBed/master/img/20200505123655.png)

**Step3：**使用mount命令挂在磁盘，例如：

```bash
sudo mount -t ext4 /dev/sdb1 /home/maxma/nlp
```

> 这一步很关键哦，～～

**Step4：**设置分区开机自动挂载，开机加载硬盘的引导文件是在`/etc/fstab`中，注意该文件只能在root权限下进行编辑，将上面挂载的硬盘添加到`fstab`文件：

```
/dev/sdb1 /home/maxma/nlp ext4 defaults 0 1
```

对于上面各个字段的含义：

> 第二个字段：挂载点；
>
> 第三个字段：文件系统名称，默认文件系统是 ext4；
>
> 第四个字段：挂载参数，这个参数和 mount 命令的挂载参数一致，defaults；
>
> 第五个字段：“指定分区是否被 dump 备份”，0 代表不备份，1 代表备份，2 代表不定期备份。
>
> 第六个字段：“指定分区是否被 fsck 检测”，0 代表不检测，其他数字代表检测的优先级，1 的优先级比 2 高。所以先检测 1 的分区，再检测 2 的分区。一般分区的优先级是 1，其他分区的优先级是 2。


# 加速git-clone

> 参考资料：https://blog.51cto.com/11887934/2051323

尝试了过用走代理来加速git，但是好像并没有成功，就还是用这种比较原始的方法来搞定吧。

## 前言

git clone（有些地区较快，有些地区较慢）；但总体来说,基本都在10KiB/s-40KiB/s之间。
作为linux运维人员来讲，经常需要在服务器上git clone；分享给大家个加速小办法，亲测有效！

## 设置

linux 修改host文件，将如下内容添加至hosts文件中： /etc/hosts

```
151.101.72.249 github.global.ssl.fastly.net  
192.30.253.112 github.com
```

如下图：

![](https://raw.githubusercontent.com/anxiang1836/FigureBed/master/img/20200505120619.png)

亲测，速度可以从几十K提升到MB的量级～～
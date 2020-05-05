# 解压命令小结

> 参考资料：https://www.cnblogs.com/cursorhu/p/5891699.html

Linux下常见的压缩包格式有5种

- zip 
- tar.gz 
- tar.bz2 
- tar.xz 
- tar.Z

其中tar是种打包格式；gz和bz2等后缀才是指代压缩方式：gzip和bzip2

**从1.15版本开始tar就可以自动识别压缩的格式,故不需人为区分压缩格式就能正确解压**，所以，解压的命令为：

```bash
tar -xvf filename.tar.gz
tar -xvf filename.tar.bz2
tar -xvf filename.tar.xz
tar -xvf filename.tar.Z
```

这里参数解释为：

`x`：e**x**tract  解压

`v`：**v**erbose 详细信息

`f`：**f**ile(file=archieve) 文件
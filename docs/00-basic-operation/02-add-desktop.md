# Linux添加程序到应用列表

> 参考资料：https://blog.csdn.net/jack_purple/article/details/54744074

## 应用背景

 下载的understand解压后执行文件每次都要切换到所在目录再用teminal ./understand打开，很麻烦，想搞一个桌面图标一类的快捷启动方式。

## 解决方法

在`/usr/share/applications`目录下创建一个桌面图标文件，名为`understand.desktop`

内容为：

```
[Desktop Entry]
Version=1.0
Name=understand
Exec=/root/Downloads/Understand/scitools/bin/linux64/understand
Terminal=false
Icon=/root/Downloads/Understand/scitools/bin/linux64/2333.png
Type=Application
Categories=Development
```

按需要修改Name,Exec,Icon项即可(Exec即为Terminal中输入的命令行)
# 更新pip源

豆瓣源是我目前为止用的比较好用的pip源，速度嗷嗷快，这里给出更新pip源为豆瓣源的方法。

在linux系统中，在`~/`目录下新建文件夹`.pip`，并新建编辑`pip.conf`文件，加入如下内容：

```
[global]
index-url = https://pypi.douban.com/simple
```

即可将pip源更新至豆瓣源
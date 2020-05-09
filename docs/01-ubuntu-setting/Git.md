# 安装Git

## 1. terminal安装Git

> 安装git：https://git-scm.com/book/zh/v2/%E8%B5%B7%E6%AD%A5-%E5%AE%89%E8%A3%85-Git

## 2. 生成SSH Key

**Step1：**设置用户名和email

```bash
git config --global user.name "zhucaixiang"
git config --global user.email "xxxx@qq.com"
```

**Step2：**生成ssh key

ssh-keygen -t rsa -C "xxxx@qq.com"

注意下输出的信息，可以看出.pub在哪个路径

复制里面的信息，粘贴到git的ssh key 中
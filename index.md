---
title: Welcome to my blog, this is my first try !
date: 2024-12-12
---

# 我是测试的文章

# Zellij安装
```bash
1、下载
cd /usr/local/src
wget https://github.com/zellij-org/zellij/releases/download/v0.41.2/zellij-x86_64-unknown-linux-musl.tar.gz

2、解压
tar -xvf zellij-x86_64-unknown-linux-musl.tar.gz
``` 

# 设置环境变量
```bash
1、编辑环境变量1
vim /etc/environment
向文件中增加内容：:/usr/local/src
结果如下：PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/usr/local/src"

2、使环境变量生效
source /etc/environment

3、设置环境变量2和别名
vim ~/.bashrc
增加如下内容：
export PATH="/usr/local/src/zellij:$PATH"
alias zj="zellij"

4、使环境变量生效
source ~/.bashrc
```

# 一些快捷键
我这里用zj替代了zellij

## 查看帮助
zj --help
## 锁定
Ctrl + g
## 面板操作：Pane
Ctrl + p
### 新建
n
### 关闭（删除）
x
### 移动
hjkl或者方向键
### 重命名
c
### 全屏
f

## 标签操作：Tab
Ctrl + T
### 新建
n
### 关闭（删除）
x
### 移动
hjkl或者方向键
### 重命名
r

## 退出面板（后台运行程序）
先Ctrl + o，然后按d

## 关闭面板（停止运行程序）
Ctrl + q

## 创建某个会话
zj -s zj2

## 查看创建的会话
> ls是list-sessions的缩写

zj ls


## 连接某个会话
> a是attach的缩写

zj a zj2

## 删除某个会话
> k是kill的缩写

zj k zj2

## 终端操作
### 复制
Shift + Insert

### 来到命令的行首
Ctrl + a

### 来到命令的行尾
Ctrl + e

### 删除当前光标至行尾的字符
Ctrl + k

### 删除当前光标至行首的字符
Ctrl + u

### 删除整行
先Ctrl + a，再Ctrl + k
或
先Ctrl + e，再Ctrl + u

### 删除光标的前一个单词
Ctrl + w

### 取消命令
Ctrl + c





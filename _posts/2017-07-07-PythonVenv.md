---
layout:     post
title:      Python 3.4+ & Virtual env
subtitle:   "Python Virtual Environment"
date:       2017-07-07 02:02:00
author:     "Sh7ne"
header-img: "img/post-bg-000.jpg"
catalog: true
tags: Python Venv Tutorial draft
---

# Python 3.4+ & Virtual env
![Python logo](https://www.python.org/static/img/python-logo.png)
#  Python Virtual Environment

### 这是一个给小白的虚拟环境傻瓜使用指南

Python 3.3 之后自带了 Virtual Environment， 就不必再去pip install virtualenv 用法实际上还是一样的。

这里的 Virtual Environment 之后用 Venv 代替。

虚拟环境，就是为了防止各种 package 冲突， 在不同的任务中用不同的虚拟环境来达到彼此分离的目的。

既然是Python 3.3 之后就自带了 Venv， 为什么标题是 Python 3.4+呢，这是因为 3.3 八本自带的 Venv 默认并没有安装 pip ， 仍需手动安装，其实就这么点区别，3.4 之后就改进了，默认自带，方便之后的操作。3.6 之后的生成语句稍有变化，之后的版本肯定以此为准，本文也按照 3.6 版本语法为例。

### 先写中文的 在 Posix 环境下 (Mac, Linux, Unix) 的，cd 到自己的 Project 目录下

# 如何生成

```python
python3 -m venv env  # create new environment in "env" folder
```
这里的 env 是自己定义的你的 Venv 的名字，也是创建的文件夹名称

下面 Activate Venv

```python
source env/bin/activate # Active Venv "env"
```

成功 Activate Venv 后，Terminal 的用户名前会自动加上 (env) 你的名字

```
    (env) User: Project User$:
```

此时就可以愉快的使用各种 pip 了， 我们可以 Run 一下

```ruby
    pip --version  # Version of pip & Python
```

可以看到 Venv中的 pip 是 Venv 中的， 并且版本是与用来生成 Venv 的 Python 版本一致。

查看目前安装了的 dependencies

```python
    pip freeze  # No output - new environment
```
第一次运行肯定是没结果的，因为环境是新建的。

下面安装之前生成的 requirements.txt
```python
    pip install -r requirements.txt # Install project dependencies
```
在用完 Venv 后，Deactivate 的方式也非常简单，直接相同目录下运行

```
    deactivate
```


先就这样，望多交流。

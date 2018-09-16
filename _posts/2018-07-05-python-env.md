---
layout: post
title: Python Windows 环境搭建
categories: Python
description: Python Windows 环境搭建
keywords: Python 环境
---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Python Windows 环境搭建**

- [Python 开发环境git](#python-%E5%BC%80%E5%8F%91%E7%8E%AF%E5%A2%83git)
  - [windows 安装pip环境](#windows-%E5%AE%89%E8%A3%85pip%E7%8E%AF%E5%A2%83)
  - [安装setuptools](#%E5%AE%89%E8%A3%85setuptools)
  - [下载pip安装包](#%E4%B8%8B%E8%BD%BDpip%E5%AE%89%E8%A3%85%E5%8C%85)
  - [解压压缩包](#%E8%A7%A3%E5%8E%8B%E5%8E%8B%E7%BC%A9%E5%8C%85)
  - [Python 排版风格](#python-%E6%8E%92%E7%89%88%E9%A3%8E%E6%A0%BC)
- [Python 2,3 版本兼容](#python-23-%E7%89%88%E6%9C%AC%E5%85%BC%E5%AE%B9)
  - [下载地址](#%E4%B8%8B%E8%BD%BD%E5%9C%B0%E5%9D%80)
  - [添加环境变量](#%E6%B7%BB%E5%8A%A0%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F)
  - [修改名字](#%E4%BF%AE%E6%94%B9%E5%90%8D%E5%AD%97)
  - [安装 pip](#%E5%AE%89%E8%A3%85-pip)
  - [验证版本](#%E9%AA%8C%E8%AF%81%E7%89%88%E6%9C%AC)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Python 开发环境git
## windows 安装pip环境
## 安装setuptools
+ 下载网址：```https://pypi.org/project/setuptools/```

## 下载pip安装包
+ 下载网址：```https://pypi.python.org/pypi/pip```

## 解压压缩包
+ 到pip解压缩目录，执行```python setup.py install```
+ 添加环境变量```C:\Python27\Scripts```
+ 命令行下执行```pip```测试

## Python 排版风格
``` python
pip install autopep8
```
# Python 2,3 版本兼容

## 下载地址
[Python 3.7.0](https://www.python.org/ftp/python/3.7.0)

[Python 2.7.11](https://www.python.org/ftp/python/2.7.11)

## 添加环境变量
这里默认安装目录如下：
```
C:\Python34\;C:\Python34\Scripts;C:\Python27\;C:\Python27\Scripts;
```
## 修改名字
这里我们只改变 Python3,Python2的保持为 python 调用
```
python.exe -> python3.exe
pythonw.exe -> pythonw3.exe
```
## 安装 pip
```
python -m pip install --upgrade pip --force-reinstall
python3 -m pip install --upgrade pip --force-reinstall
```
## 验证版本
```
pip2 -V
pip3 -V
```
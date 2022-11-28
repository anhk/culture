---
layout: post
title: 压缩Golang可执行程序
---

通常golang的可执行程序普遍尺寸比较大，这里总结了压缩Golang可执行程序，缩减尺寸的方法。

<!--more-->

## 编译及压缩

**标准编译后的程序尺寸：**
```bash
$ ls -al myprogram
-rwxr-x--- 1 anhk anhk 378653100 11月 28 12:56 myprogram
$
```

**调整编译选项：**
```bash
$ ls -al myprogram
-rwxr-x--- 1 anhk anhk 172497792 11月 28 12:57 myprogram
$
```

> `​go build -ldflags="-s -w"`  -s：省略符号表和调试信息； -w: 省略 DWARF 消息


**使用upx压缩：**
```bash
$ upx myprogram
                       Ultimate Packer for eXecutables
                          Copyright (C) 1996 - 2020
UPX 3.96        Markus Oberhumer, Laszlo Molnar & John Reiser   Jan 23rd 2020

        File size         Ratio      Format      Name
   --------------------   ------   -----------   -----------
 172497792 ->  44140552   25.59%   linux/amd64   myprogram

Packed 1 file.
```

## 安装UPX

### CentOS
```bash
$ sudo yum -y install upx
```


### Ubuntu
```bash
$ sudo apt -y install upx-ucl
```


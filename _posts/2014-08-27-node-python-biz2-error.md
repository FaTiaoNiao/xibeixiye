---
date: 2014-08-27 00:14:31+00:00
layout: post
title: 由于Python缺少bz2库而导致node安装失败
categories: 开发笔记
tags: node.js python2.7 bz2 CentOS6.4
---
我的VPS使用的是CentOS6.4 64bit版本，系统自带的python版本为2.6.6，使用编译源代码的方法将其升级到2.7.5版本，yum依然使用2.6.6版本。但在安装node.js时在make这一步中报错：

        Traceback (most recent call last):  
        File "../../tools/js2c.py", line 36, in <module>  
        import bz2  
        ImportError: No module named bz2  
        make[1]: *** [/home/softs/node-v0.8.12/out/Release/obj/gen/libraries.cc] Error 1  
        make[1]: Leaving directory `/home/softs/node-v0.8.12/out'  
        make: *** [node] Error 2

这是由于没有安装bz2所致，首先安装bz2库：

         yum install -y bzip2*

然后找到刚才编译安装Python时的源代码的目录，进入zlib模块的目录，编译安装：
        
        $cd /usr/local/src/Python-2.7.5/Modules/zlib
        $./configure   
        $make && make install

然后回退到python源码目录，安装模块：

        $cd /usr/local/src/Python-2.7.5/    
        $python setup.py install

然后重新编译安装node就可以了。

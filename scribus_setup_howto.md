# Introduction #
fullcircle中文排版使用的是Scribus软件。本页面介绍了scribus安装的以下问题：
  1. 从哪里获取scribus
  1. 如何用二进制方式安装
  1. 如何用源代码方式安装
  1. 如何安装scribus的不同版本


## 从哪里获取scribus ##
scribus的官方网站是www.scribus.net，它提供了帮助文档http://docs.scribus.net和软件下载链接http://www.scribus.net/downloads。
scribus能支持Linux,windows,mac OS等多个平台。你可以在http://www.scribus.net/downloads获得安装包和源代码包。

## 如何用二进制方式安装 ##
  1. linux:
Arch Linux用户请用pkgbuild(参照http://aur.archlinux.org/packages.php?ID=16640)
Ubuntu(10.4/10.10)用户请通过以下PPA方式安装：……待补充。

  1. windows:
请参考http://wiki.scribus.net/canvas/Download页面的Download Scribus 1.3.9 installer for Windows (32-bit)。

  1. mac OS:

## 如何用源代码方式安装 ##
请参考：http://wiki.scribus.net/index.php/Building_SVN_versions_with_CMake
  1. 稳定版1.3.3.x源码编译安装：
```
svn co svn://scribus.info/Scribus/branches/Version133x/Scribus scribus133x
cd ./scribus133x
cmake -DCMAKE_INSTALL_PREFIX:PATH=/path/to/your/installdir/
make
sudo "make install"
```
这样会把 branches/Version133x的源码（如1.3.3.14)，编译后安装到你 /path/to/your/installdir/ 路径下。
  1. NG版安装(排版组目前NG版为1.4.0svn)
```
wget https://launchpad.net/~fcctt-clt/+archive/staging/+files/scribus-fcctt_1.3.9%2Bsvn20110125.orig.tar.bz2
tar -zjvf scribus-fcctt_1.3.9+svn20110125.orig.tar.bz2
cd ./scribus-fcctt-1.3.9+svn20110125
cmake -DCMAKE_INSTALL_PREFIX:PATH=/path/to/your/installdir/
make
sudo "make install"
```

## 安装限制 ##
  1. 目前scribus-fcctt的PPA只提供ubuntu 10.4和10.10的安装功能。ubuntu 9.10或更低版本用户，请通过源码编译安装。
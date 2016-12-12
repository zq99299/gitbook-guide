# 1.1. 安装
## 运行环境
现在大多数软件都依赖Node.js了，所以需要先安装node和 npm；
解决被墙的一个方法就是安装淘宝的cnpm
```
$ npm install -g cnpm --registry=https://registry.npm.taobao.org 
```
使用方式只是把npm 改为了cnpm，能加快一些npm市场中的安装，但是也不能解决安装之后具体软件从自己服务器下载文档的速度。

## 安装gitbook cli
```vim
$ npm install -g gitbook-cli

```
gitbook-cli 是gitbook的命令行操作工具，它封装了一系列的命令，包括书籍初始化、预览、构建等等操作。 

第一次安装 gitbook-cli 之后，还会自动安装最新版的gitbook应用程序。我们之前说 gitbook-cli 只是一个命令行工具，仅有 gitbook-cli 还不够，我们还需要安装gitbook程序。 

由于网络因素，可能第一次安装gitbook会较慢，因为它的安装过程是先下载gitbook的源码，然后在本地编译。这个编译过程是依赖node-gyp的。

在安装gitbook完成之后，我们可以使用 gitbook versions 来查看当前已经安装的gitbook版本，

```
$ gitbook init
```
书籍初始化:该过程可能会激活下载最新的gitbook程序。
其实安装 gitbook cli 和 gitbook 才算真正完成了安装。


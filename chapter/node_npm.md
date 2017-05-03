# NPM相关配置
* 缓存目录修改
* 镜像更换
* 安装cnpm


## 安装node
https://nodejs.org/en/
1. 下载6.+版本
2. 点击安装，在安装的时候，有一项是AddPath；
	该项是默认的，如果以后遇到使用npm安装软件之后，提示命令找不到，那么去配添加下全局路径中的 node_global\node_modules 在path中。

## linux 安装
https://nodejs.org/en/download/

1. 下载 linux 版本的，如：node-v6.10.0-linux-x64.tar.xz
2. 解压  tar xvJf node-v6.10.0-linux-x64.tar.xz （两层压缩，外层xz。内层tar）
3. 设置为全局

```bash
ln -s /home/kun/mysofltware/node-v6.10.0-linux-x64/bin/node /usr/local/bin/node
ln -s /home/kun/mysofltware/node-v6.10.0-linux-x64/bin/npm /usr/local/bin/npm

/home/kun/mysofltware 为你的安装目录的上级目录
```



## 修改配置文件
C:\Users（用户）\你的用户名\.npmrc 这个文件中
```
prefix=e:\node\node-global
cache=E:\node\node-cache
registry = http://registry.cnpmjs.org 
```
以上文件名需要注意，最好不要有中文和空格，否则会出现，输入npm命令无任何反应

## 命令行修改
配置npm的全局模块存放路径和cache路径 
```bash
npm config set prefix “D:\Program Files\node\node-global” 
npm config set cache “D:\Program Files\node\node-cache” 

## 安装cnpm
npm install cnpm -g
cnpm config set prefix “D:\Program Files\node\node-global” 
cnpm config set cache “D:\Program Files\node\node-cache”
```

## 如果出现命令无效
那么先看全局路径所在的位置，然后该该路径添加到环境变量Path中
```bash
npm root -g
```
`注意：`在安装node的时候好像会添加一个默认路径到环境变量中，需要更改掉该路径，不然你用到的都是以前的，但是下载安装的却是现在的。如图：

![](/images/node-npm-path.jpg)

如果你配置的是以下路径，那么path里面就应该写：D:\Program Files\node\node-global
```
npm config set prefix “D:\Program Files\node\node-global” 
```


linux 下：
```bash
vim /etc/profile
export NODE_MODULES=/mnt/xx/app/node/node-global/bin
export PATH=$NODE_MODULES

再刷新 ： source /etc/profile
```

## npm更新到最新版本的方法
1. 查询当前已按照版本
```bash
npm -v
```
2. 安装最新的版本到当前目录下
```bash
npm i npm g 
运行完成之后会出现以下目录：
|- node_modules
|-- .bin
|-- g
|-- npm
这里的npm就是最新的npm包。
```

## npm更新：另外一个命令
```bash
npm update -g
```

4. 删除并覆盖远文件夹
把下载下来的npm文件夹复制到nodejs的安装目录下 
我是按照到e盘的： `e:\nodejs\node_modules`
要先删除该文件夹已有的npm文件夹。


## 插件发布到npm社区
1. www.npmjs.org 注册自己的账户
2. 添加账户注册的信息
```bash
$ npm adduser	
Username: your name
Password: your password
Email: yourmail
```
npm会把认证信息存储在~/.npmrc中，并且可以通过以下命令查看npm当前使用的用户：$ npm whoami 
3. 推送到npm社区
```bash
进入插件所在目录，
npm publish
```
4. 卸载一个模块
```bash
npm uninstall
```
5. 撤销一个发布
```bash
npm unpublish 模块@版本
如：
npm unpublish gitbook-plugin-anchor-navigation-ex@1.2.1
```


# NPM相关配置
* 缓存目录修改
* 镜像更换
* 安装cnpm

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


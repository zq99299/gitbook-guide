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
```
npm config set prefix “D:\Program Files\node\node-global” 
npm config set cache “D:\Program Files\node\node-cache” 

## 安装cnpm
npm install cnpm -g
cnpm config set prefix “D:\Program Files\node\node-global” 
cnpm config set cache “D:\Program Files\node\node-cache”
```

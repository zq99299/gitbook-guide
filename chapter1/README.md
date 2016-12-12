# 1.GitBook的安装与入门
Gitbook 是基于 Node.js 的命令行工具，用来创建漂亮的电子书，它使用 Markdown 或 AsciiDoc 语法来撰写内容，用 Git 进行版本控制，且可以托管在 Github 上。Gitbook 可以将作品编译成网站、 PDF、 ePub 和 MOBI 等多重格式。

如果你不擅长自己搭建 gitbook 环境，还可以使用 gitbook.com 在线服务来创建和托管你的作品，他们还提供了基于桌面的 编辑器 。 

# node 模块安装目录配置
4.配置npm的全局模块存放路径和cache路径 
 输入以下命令 
```
npm config set prefix “D:\Program Files\node\node-global” 
npm config set cache “D:\Program Files\node\node-cache” 
```
5.安装cnpm

在cmd下输入命令： 
```
npm install cnpm -g
```
6.设置cnpm的全局模块存放路径和cache路径 
```
cnpm config set prefix “D:\Program Files\node\node-global” 
cnpm config set cache “D:\Program Files\node\node-cache”
```
以后npm和cnpm安装的模块就都在D:\Program Files\node\node-global\node_modules这个目录下了。


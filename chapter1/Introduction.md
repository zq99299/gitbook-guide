# 1.2.入门
在你的作品目录中创建两个必需的文件 README.md 和 SUMMARY.md，README.md 是作品的介绍，SUMMARY.md 是作品的目录结构，里面要包含一个章节标题和文件索引的列表：

```
# Summary

This is the summary of my book.

* [section 1](section1/README.md)
    * [example 1](section1/example1.md)
    * [example 2](section1/example2.md)
* [section 2](section2/README.md)
    * [example 1](section2/example1.md)
```
根据 SUMMARY.md 的目录结构初始化各个章节文件：
```
$ gitbook init
```
运行服务，在编辑内容后实时预览：
```
$ gitbook serve
```
服务器启动后，浏览器打开 http://localhost:4000 查看，撰写完后可以生成静态网站用来发布：
```
$ gitbook build
```

以上方式使用命令行来运行，基于客户端的经过我的尝试，貌似没有发现有以上的功能，所以需要生成文件什么的还是需要通过命令行方式


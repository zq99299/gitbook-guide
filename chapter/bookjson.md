# 配置

记录Gitbook的一些配置信息
在book.json 中配置以下信息
* title - 标题
* author - 作者信息
* description - 书本描述
* language - 使用的语言
* links - 在侧边栏添加链接
* styles - 自定义样式
* plugins - 插件
* pluginsConfig - 插件配置
* gitbook - 指定gitbook版本

## title

设置书本的标题
```json
"title" : "Gitbook Use"
```

## author

作者的相关信息
```json
"author" : "zhangjikai"
```

## description

本书的简单描述
```json
"description" : "记录Gitbook的配置和一些插件的使用"
```

## language

Gitbook使用的语言, 版本2.6.4中可选的语言如下：

en, ar, bn, cs, de, en, es, fa, fi, fr, he, it, ja, ko, no, pl, pt, ro, ru, sv, uk, vi, zh-hans, zh-tw
配置使用简体中文
```json
"language" : "zh-hans",
```

## links

在左侧导航栏添加链接信息
```json
"links" : {
    "sidebar" : {
        "Home" : "http://zhangjikai.com"
    }
}
```

## styles

自定义页面样式， 默认情况下各generator对应的css文件
```json
"styles": {
    "website": "styles/website.css",
    "ebook": "styles/ebook.css",
    "pdf": "styles/pdf.css",
    "mobi": "styles/mobi.css",
    "epub": "styles/epub.css"
}
```

例如使`<h1> <h2>`标签有下边框， 可以在website.css中设置

```css
h1 , h2{
    border-bottom: 1px solid #EFEAEA;
}
```

## plugins

配置使用的插件
```json
"plugins": [
    "disqus"
]
```
添加新插件之后需要运行gitbook install来安装新的插件

Gitbook默认带有5个插件：

* highlight
* search
* sharing
* font-settings
* livereload

如果要去除自带的插件， 可以在插件名称前面加-

```json
"plugins": [
    "-search"
]
```

## pluginsConfig

配置插件的属性
```json
"pluginsConfig": {
    "fontsettings": {
        "theme": "sepia",
        "family": "serif",
        "size":  1
    }
}
```

## gitbook

指定使用的gitbook版本

```json
"gitbook" : "2.6.4",
```


# book.json

```json
{
    "title" : "Gibook Use",
    "description" : "记录Gitbook的配置和一些插件的使用",
    "author" : "zhangjikai",
    "generator": "site",
    "language" : "zh-hans",
    "gitbook" : "2.6.4",
    "links" : {
        "sidebar" : {
            "Home" : "http://zhangjikai.com"
        }
    },
   "plugins": [
        "disqus",
        "-search",
        "search-pro@1.0.7",
        "advanced-emoji@0.1.5",
        "github",
        "ace",
        "emphasize",
        "katex",
        "anchors",
        "include-codeblock",
        "mermaid",
        "tbfed-pagefooter",
        "sectionx",
        "expandable-chapters",
        "codeblock-filename",
        "baidu",
        "sitemap@1.0.2",
        "donate",
        "local-video",
        "toc",
        "edit-link"

    ],
    "pluginsConfig": {
        "disqus": {
            "shortName": "gitbookuse"
        },
        "github": {
            "url": "https://github.com/zhangjikai/gitbook-use"
        },
        "search-pro": {
            "cutWordLib": "nodejieba",
            "defineWord": ["gitbook-use"]
         },

        "sharing": {
            "weibo": true,
            "facebook": true,
            "twitter": true,
            "google": false,
            "instapaper": false,
             "vk": false,
            "all": [
                "facebook", "google", "twitter",
                "weibo", "instapaper"
            ]
        },

        "tbfed-pagefooter": {
            "copyright":"Copyright &copy zhangjikai.com 2015",
            "modify_label": "该文件修订时间：",
            "modify_format": "YYYY-MM-DD HH:mm:ss"
        },

        "baidu": {
            "token" : "ff100361cdce95dd4c8fb96b4009f7bc"
        },
        "sitemap": {
            "hostname": "http://gitbook.zhangjikai.com"
        },

        "donate": {
          "wechat": "http://zhangjikai.com/resource/weixin.png",
          "alipay": "http://zhangjikai.com/resource/alipay.png",
          "title": "",
          "button": "赏",
          "alipayText": "支付宝打赏",
          "wechatText": "微信打赏"
        },

         "edit-link": {
                "base": "https://github.com/zhangjikai/gitbook-use/edit/master",
                "label": "Edit This Page"
         }

    }
}
```

# 其他配置
## 配置pdf封面
在项目根目录下添加：
- cover_small.jpg

 大图，1800 * 2360
- cover.jpg
 小图，200 * 262
 
 
# 目录配置
默认主题有一个配置参数： 显示层级的。
```
 "theme-default": {
   "showLevel": true
 }
```

它的解析方式应该如下：

```
SUMMARY.md
 
# xxxx

* [前言](README.md)

## xxxx

* [前言](README.md)

# cc
sdfdsfdsfsd
* [前言](README.md)

============  以上是SUMMARY.md 内容 ======
解析出来在网页中的效果是：
1.1 [前言](README.md)
2.1 [前言](README.md)
sdfdsfdsfsd
3.1 [前言](README.md)

```

本书的侧边栏效果文件如下:
```
##1. Gitbook 使用笔记
* [概述](chapter/README.md)
* [安装](chapter/install.md)
* [命令](chapter/command.md)
* [配置](chapter/bookjson.md)
* [插件](chapter/plugin.md)
    * [prismjs 代码高亮](chapter/plugin/prismjs.md)
    * [ace 代码高亮编辑](chapter/plugin/ace.md)
    * [navigator 页面导航](chapter/plugin/navigator.md)
* [插件开发](chapter/dev_plugin.md)    
* [NPM相关](chapter/node_npm.md)
* [主题](chapter/theme/README.md)
    * [API](chapter/theme/api.md)
    * [FAQ](chapter/theme/faq.md)
```

> 参考链接： https://toolchain.gitbook.com/pages.html
 
 

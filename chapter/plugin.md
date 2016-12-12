<!-- toc -->

# 插件
记录一些实用的插件, 如果要指定插件的版本可以使用 `plugin@0.3.1`。下面的插件在 `GitBook 的 2.6.4版本中`可以正常工作，因为一些插件可能不会随着 `GitBook` 版本的升级而升级，即下面的插件可能不适用高版本的 `GitBook`，所以这里指定了`GitBook`的版本。另外一些插件在windows上的安装会有问题，比如 `Search Pro` 和 `Mermaid`，我也没有找到特别好的解决办法，如果有知道相关解决办法的，请不吝赐教。

* Disqus - Disqus评论
* duoshuo - 多说
* Search Pro - 支持中文搜索
* Advanced Emoji - 支持emoji表情
* Github - 添加github图标
* Ace Plugin - 支持ace
* Emphasize - 强调文字(为文字加上底色)
* KaTex - 支持数学公式
* Include Codeblock - 使用代码块显示指定文件的内容
* Splitter - 自由调节侧边栏宽度
* Mermaid -支持渲染Mermaid图表
* sharing - 分享
* Tbfed-pagefooter - 为页面添加页脚
* Toggle Chapters - 折叠章节
* Sectionx - 将页面分块显示
* Codeblock-filename - 为代码块添加文件名称
* ga - google 统计
* baidu - 百度统计
* donate - 打赏
* Local Video - 使用Video.js播放视频
* toc - 自动生成目录
* Edit Link - 链接到当前页源文件上
* sitemap - 生成sitemap

> 插件安装：由于被墙，所以不能通过配置book.json中配置文件自动下载安装，否则会很慢，使用cnpm手动全局安装好以后，会自动在缓存中获取。
```
cnpm install gitbook-plugin-插件名称
如：
cnpm install gitbook-plugin-tbfed-pagefooter
```

## anchors

标题带有 github 样式的锚点。

## github-buttons

显示 github 仓库的 star 和 fork 按钮。
https://plugins.gitbook.com/plugin/github-buttons

## prism
https://plugins.gitbook.com/plugin/prism
基于 Prism 的代码高亮。

## Disqus

添加disqus评论

[插件地址](https://plugins.gitbook.com/plugin/disqus)
```json
"plugins": [
    "disqus"
],
"pluginsConfig": {
    "disqus": {
        "shortName": "gitbookuse"
    }
}
```

## Duoshuo

添加多说

[插件地址](https://plugins.gitbook.com/plugin/duoshuo)
```json
{
    "plugins": [
        "duoshuo"
    ],
    "pluginsConfig": {
        "duoshuo": {
            "short_name": "your duoshuo's shortname",
            "theme": "default"
        }
    }
}
```

## Search Pro

支持中文搜索, 需要将默认的search插件去掉, :worried: 在window下安装该插件时总是出错 :worried:
[插件地址](https://plugins.gitbook.com/plugin/search-pro)
```json
"plugins": [
    "-search",
    "search-pro"
],
"pluginsConfig": {
    "search-pro": {
        "cutWordLib": "nodejieba",
        "defineWord" : ["Gitbook Use"]
    }
}
```

## Advanced Emoji

支持emoji表情
[emoij表情列表](http://www.webpagefx.com/tools/emoji-cheat-sheet/)
[插件地址](https://plugins.gitbook.com/plugin/advanced-emoji)
```json
"plugins": [
    "advanced-emoji"
]
```
使用示例:

:bowtie: :smile: :laughing: :blush: :smiley: :relaxed:


## Github

在顶部右上角添加github图标，点击该图标跳转到自己配置的地址
[插件地址](https://plugins.gitbook.com/plugin/github)
```json
"plugins": [ 
    "github" 
],
"pluginsConfig": {
    "github": {
        "url": "https://github.com/zhangjikai"
    }
}
```

##Ace Plugin

使gitbook支持ace
[插件地址](https://plugins.gitbook.com/plugin/ace)
```json
"plugins": [
    "ace"
]
```
使用示例:
```
// This is a hello world program for C.
#include <stdio.h>

int main(){
  printf("Hello World!");
  return 1;
}
```

## Emphasize

为文字加上底色
[插件地址](https://plugins.gitbook.com/plugin/emphasize)
```json
"plugins": [
    "emphasize"
]
```
使用示例:
```
This text is {% em %}highlighted !{% endem %}

This text is {% em %}highlighted with **markdown**!{% endem %}

This text is {% em type="green" %}highlighted in green!{% endem %}

This text is {% em type="red" %}highlighted in red!{% endem %}

This text is {% em color="#ff0000" %}highlighted with a custom color!{% endem %}
```

## include-codeblock
使用代码块的格式显示所包含文件的内容. 该文件必须存在.

[插件地址](https://plugins.gitbook.com/plugin/include-codeblock)
```json
"plugins": [
    "include-codeblock"
]
```
使用示例:
```css
/* CSS for website */
h1 , h2{
    border-bottom: 1px solid #EFEAEA;
    padding-bottom: 3px;
}


.book .book-body .page-wrapper .page-inner section.normal {
    min-height:350px;
    margin-bottom: 30px;
}

.book .book-body .page-wrapper .page-inner section.normal hr {
    height: 0px;
    padding: 0;
    margin: 1.7em 0;
    overflow: hidden; 
    background-color: #e7e7e7;
    border-bottom: 1px dotted #e7e7e7;
}

.video-js {
    width:100%;
    height: 100%;
}
```


# Splitter
使侧边栏的宽度可以自由调节

插件地址 : https://plugins.gitbook.com/plugin/splitter

![](/images/gitbook-splitter-demo.gif)

## Mermaid

支持渲染Mermaid图表

插件地址 : https://plugins.gitbook.com/plugin/mermaid
```json
"plugins": [
    "mermaid"
]
```

## Sharing

分享当前页面, gitbook的默认插件, 使用下面方式来禁用
```json
 plugins: ["-sharing"]
```
配置
```json
"pluginsConfig": {
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
    }
}
```

## Tbfed-pagefooter

为页面添加页脚

插件地址 : https://plugins.gitbook.com/plugin/tbfed-pagefooter
```json
"plugins": [
   "tbfed-pagefooter"
],
"pluginsConfig": {
    "tbfed-pagefooter": {
        "copyright":"Copyright &copy zhangjikai.com 2015",
        "modify_label": "该文件修订时间：",
        "modify_format": "YYYY-MM-DD HH:mm:ss"
    }
}
```

## Toggle Chapters

是左侧的章节目录可以折叠

插件地址 : https://plugins.gitbook.com/plugin/toggle-chapters
```json
"plugins": ["toggle-chapters"]
```

## Sectionx

将页面分块显示

插件地址 : https://plugins.gitbook.com/plugin/sectionx
```json
"plugins": [
   "sectionx"
]
```
使用示例：
<!--sec data-title="Introduction" data-id="section0" data-show=true ces-->

Insert markdown content here (you should start with h3 if you use heading).
```
本样式就是用下面的代码写出来的
<!--sec data-title="Introduction" data-id="section0" data-show=true ces-->

Insert markdown content here (you should start with h3 if you use heading).

<!--endsec-->
```
<!--endsec-->

**实际测试：** 可用性不高，内容里面并不是什么都支持，比如这里

## Codeblock-filename

为代码块添加文件名称

插件地址 : https://plugins.gitbook.com/plugin/codeblock-filename

```json
plugins: [ "codeblock-filename" ]
```
```
 \```js:test.js
  codeblock
 \```
```
```js:test.js
codeblock
```

## GA

google 统计

插件地址 : https://plugins.gitbook.com/plugin/ga
```json
"plugins": [
    "ga"
 ],
"pluginsConfig": {
    "ga": {
        "token": "UA-XXXX-Y"
    }
}
```

## Baidu

百度统计

插件地址 : https://plugins.gitbook.com/plugin/baidu 
```json
"plugin": [
    "baidu"
 ],
"pluginsConfig": {
    "baidu": {
        "token": "YOUR TOKEN"
    }
}
```

## Donate

打赏插件
插件地址
```json
"plugins": [
    "donate"
],
"pluginsConfig": {
    "donate": {
        "wechat": "http://zhangjikai.com/resource/weixin.png",
        "alipay": "http://zhangjikai.com/resource/alipay.png",
        "title": "",
        "button": "赏",
        "alipayText": "支付宝打赏",
        "wechatText": "微信打赏"
    }
}
```
## Local Video

使用Video.js 播放本地视频

插件地址: https://plugins.gitbook.com/plugin/local-video
```json
"plugins": [ "local-video" ]
```

## Toc

自动生成本页的目录结构，一般情况下生成的目录是正常的，但是可能会与其他插件冲突，造成生成的目录不正确.

插件地址 : https://plugins.gitbook.com/plugin/toc
下面的 pluginsConfig用来给ul添加css样式
```json
"pugins": [
    "toc"
],
"pluginsConfig": {
    "toc": {
        "addClass": true,
        "className": "toc"
    }
}
```
使用方法: 在需要生成目录的地方加上 <!-- toc -->

## Edit Link

如果将gitbook的源文件保存到github或者其他的仓库上，使用该插件可以链接到当前页的源文件上。

插件地址:https://plugins.gitbook.com/plugin/edit-link

```json
"plugins": ["edit-link"],
"pluginsConfig": {
    "edit-link": {
        "base": "https://github.com/USER/REPO/edit/BRANCH",
        "label": "Edit This Page"
    }
}
```

## Sitemap

生成sitemap

插件地址 : https://plugins.gitbook.com/plugin/sitemap
```json
{
    "plugins": ["sitemap@1.0.2"],
    "pluginsConfig": {
        "sitemap": {
            "hostname": "http://mybook.com/"
        }
    }
}
```
使用1.1.0生成的xml文件有些问题, 所以这里使用1.0.2版本

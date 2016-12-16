# 插件
只简要记录一些觉得还可以的插件。

在使用非官方插件的时候，你就要做好心里准备：
* 可能不会随着gitbook的升级而升级
* 每个开发者都有自己的开发习惯，所以插件很有可能和其他插件冲突，导致失效

分享个寻找插件的方法：所谓插件是符合自己需求的才是最好的，https://plugins.gitbook.com/ 官网插件库，该库会自动拉取npm 中 gitbook-plugin- 前缀的插件。

1. 根据名称寻找你需求的插件
2. 查看详细描述，如果觉得还ok，就自己尝试测试下效果，这样寻找插件是最好的。
3. 如果一个插件有bug或则不太符合你的需求，那么你需要修改这个插件并发布到npm仓库，相当于自己写了一个插件。至于怎么写一个插件，最好的方法就是，找一个比较简单的插件看他的写法


> 插件安装：由于被墙，所以不能通过配置book.json中配置文件自动下载安装，否则会很慢，使用cnpm手动安装，再使用 gitbook install
```
cnpm install gitbook-plugin-插件名称
如：
cnpm install gitbook-plugin-tbfed-pagefooter
```

## 个人觉得必须实用的插件
* [4.1. prismjs 代码高亮](plugin/prismjs.md) `★★★★★`
* [anchors 标题带有 github 样式的锚点](https://plugins.gitbook.com/plugin/anchors) `★★★★★`
* [anchor-navigation-ex 自用修复navigator插件相关bug和增加功能](https://github.com/zq99299/gitbook-plugin-anchor-navigation-ex) `★★★★★`
* [Splitter 使侧边栏的宽度可以自由调节](https://plugins.gitbook.com/plugin/splitter)`★★★★★`
* [expandable-chapters 目录折叠](https://github.com/DomainDrivenArchitecture/gitbook-plugin-expandable-chapters)`★★★★★`
* [Tbfed-pagefooter 为页面添加页脚修改时间](https://plugins.gitbook.com/plugin/tbfed-pagefooter) `★★★★★`


## 还可以但是不是必须的插件

* [4.2. ace 代码高亮编辑](plugin/ace.md)
* [4.3. navigator 页面导航](plugin/navigator.md) `★★★`
* [page-footer 页脚添加信息](https://github.com/aleen42/gitbook-footer) `★★★★★`
* [bootstrap-callout 多风格样式标注](https://github.com/getredash/gitbook-plugin-bootstrap-callout) `★★★★★`
* [autocover 封装生成](https://plugins.gitbook.com/plugin/autocover) `★★★★★`



--------


# 没有尝试或则尝试失败的插件
## styles-sass

使用 SASS 替换 CSS。
https://plugins.gitbook.com/plugin/styles-sass

## styles-less

使用 LESS 替换 CSS。
https://plugins.gitbook.com/plugin/styles-less

## book-summary-scroll-position-saver

自动保存左侧目录区域导航条的位置。

https://plugins.gitbook.com/plugin/book-summary-scroll-position-saver

**实际测试：** 暂时没有发现有什么用处，貌似也没有什么效果



## github-buttons

在右上角显示 github 仓库的 star 和 fork 按钮。
https://plugins.gitbook.com/plugin/github-buttons
```json
"github-buttons": {
      "repo": "zq99299/gitbook-guide",  // 不需要https://github.com/前缀
      "types": [
        "star",
        "watch"
      ],
      "size": "small"
    }
```
**实际测试：** 由于访问github，载入速度会拖垮一大截



## Disqus disqus评论

插件地址 ：https://plugins.gitbook.com/plugin/disqus

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

## Duoshuo 多说

插件地址 ： https://plugins.gitbook.com/plugin/duoshuo

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

## Search Pro 支持中文搜索

支持中文搜索, 需要将默认的search插件去掉, :worried: 在window下安装该插件时总是出错 :worried:
插件地址 ：https://plugins.gitbook.com/plugin/search-pro 

使用该插件必须安装：
* 1) 安装 .NET Framework 2.0 SDK；（400多m安装包）
* 2) 安装 Microsoft Visual Studio 2005；（1.5g安装包）

## autocover 封装生成 

https://toolchain.gitbook.com/ebook.html

https://plugins.gitbook.com/plugin/autocover

使用该插件必须安装：
* 1) 安装 .NET Framework 2.0 SDK；（400多m安装包）
* 2) 安装 Microsoft Visual Studio 2005；（1.5g安装包）

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


## Github 顶部右上角添加github图标

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
## include-codeblock 使用代码块显示指定文件的内容
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


## Mermaid

支持渲染Mermaid图表

插件地址 : https://plugins.gitbook.com/plugin/mermaid
```json
"plugins": [
    "mermaid"
]
```

## Sharing 分享图标

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
**实际测试：** 并没有插件中显示的效果

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

## bootstrap-callout 多风格样式标注

> #### primary:: primary Title
>
> 测试

用空行隔开多个标注还不行

> #### success:: success Title
>
> 测试

只能使用文字隔开？或则分割线？

> #### danger:: danger Title
>
> 测试

---

> #### warning:: warning Title
>
> 测试

---

> #### info::Title
>
> 测试

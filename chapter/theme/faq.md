# FAQ 主题

该主题的网站展示样式就和普通的book不一致了。

`官网插件`https://github.com/GitbookIO/theme-faq#readme

`效果预览`https://zq99299.gitbooks.io/gitbook-faq-demo/content/
## 添加logo

```
// 这一句话本来也有{%%}包括起来的，但是运行gitbook serve 报错，只好去掉了
extends template.self

{% block faq_header_brand %}
<img src="http://www.mrcode.cn/assets/img/depots/zhuqiang/blog_show.png" height="30" />
{% endblock %}
```

## 添加导航

```
extends template.self


{% block faq_menu %}
<ul class="nav navbar-nav navbar-right">
    <li><a href="#">导航添加测试1</a></li>
    <li><a href="#">导航添加测试2</a></li>
</ul>
{% endblock %}

```


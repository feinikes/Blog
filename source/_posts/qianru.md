---
title: 嵌入JavaScript脚本的位置
date: 2016-12-14 20:14:37
tags: [JavaScript]
---
>JavaScript脚本代码可放在HTML文档任何需要的位置。一般来说，可以在< head>与< /head>标记对、< body>与< /body>标记对之间按需要放置JavaScript脚本代码。

放置在< head>与< /head>标记对之间
---
放置在< head>与< /head>标记对之间的JavaScript脚本代码一般用于提前载入以响应用户的动作，一般不影响HTML文档的浏览器显示内容。如下是其基本文档结构：
``` bash
<html>
<head>
<title>放置在<head>与</head>标记对之间</title>
<!-- 直接写JavaScript代码 -->
<script type="text/javascript">
    // JavaScript 代码
</script>
<!-- 引入外部脚本 -->
<script type="text/javascript" src="1-2.js"></script>
</head>
<body>
</body>
</html>
```
放置在<body>与</body>标记对之间
---
JavaScript脚本也可以放置在< body>与< /body>标记对之间，可根据需要编写多个独立的脚本代码段并与HTML代码结合在一起。
```bash
<html>
<head>
<title>放置在<body>与</body>标记对之间</title>
</head>
<body>
<!-- 直接写JavaScript代码 -->
<script type="text/javascript">
    // JavaScript 代码
</script>
<!-- 引入外部脚本 -->
<script type="text/javascript" src="1-2.js"></script>
</body>
</html>
```
>注意：在< head>和< body>标签内可以有多个代码块，只要放在< script type="text/javascript">与< /script>之间或者引入外部脚本即可。同时，JavaScript脚本也可以放在其他任意HTML标签之间，如< div>、< p>、< span>等。

说明：浏览器一般是从上到下渲染HTML，当遇到Javascript代码时，浏览器将发生阻塞（不再解析后边的任何代码，包括JavaScript和HTML），有些浏览器在阻塞期间不会解析该Javascript代码后边的HTML代码，必须等到该Javascript代码执行完毕，才继续解析。如果将Javascript放置在< head>...< /head>或者< body>...< /body>之间，经常会发生这种现象：浏览器先是呈现一部分页面，再呈现后边的页面，中间间隔时间明显。这样带来的明显结果就是用户体验差。

因此，如无特殊需求，我们强烈建议将JavaScript代码置于< body>...< /body>的最后。如：
```bash
<body>
<!-- HTML代码 -->
<script type="text/javascript">
    // Javascript代码
</script>
<script type="text/javascript" src="1-2.js"></script>
</body>
```
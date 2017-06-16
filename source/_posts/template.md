---
title: 原生的模板引擎
date: 2017-03-03 17:30:43
tags: [template,引擎]
---
### 代码
```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8"/>
    <title>原生的模板引擎</title>
</head>

<body style="background: white; ">
<h1>原生的模板引擎</h1>
<script type="text/tempalte" id="tmpl">
        <% name %>，<% age %>岁，在 <% company %> 上班
</script>
<script>
    // 创建对象
    var obj = {
        "name": "张展",
        "age": 30,
        "company": "乾康金融"
    }
    // 把上面的obj中的数据绑定到tmpl中,输出完整的一句话
    // 正则 认识<% value %>格式
    var reg = /<%\s*([^%>]\S+)\s*%>/;

    function tempalte(id, obj) {
        var html = document.getElementById(id).innerHTML;
        // 初始化
        var _exec = null;
        while (_exec = (reg.exec(html))) {
            html = html.replace(_exec[0], obj[_exec[1]]);
        }
        return html;
    }
    document.write(tempalte('tmpl', obj))
</script>
</body>
</html>
```
### 效果

张展，30岁，在 乾康金融 上班

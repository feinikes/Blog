---
title: 快贷前端书写规则
date: 2016-12-27 18:22:18
tags: [Web,快贷]
---
1.面包屑
---
```bash
<h3>
    Dashboard
</h3>
<ul class="breadcrumb">
    <li>
        <a href="#">Dashboard</a>
    </li>
    <li class="active"> My Dashboard </li>
</ul>
```
2.左侧导航
```bash
<ul class="nav nav-pills nav-stacked custom-nav">
    <li class="active"><a href="index.html"><i class="fa fa-home"></i> <span>我的工作台</span></a></li>
    <li class="menu-list"><a href=""><i class="fa fa-laptop"></i> <span>客户管理</span></a>
        <ul class="sub-menu-list">
            <li><a href="blank_page.html"> 新建客户</a></li>
            <li><a href="boxed_view.html"> 客户信息查询</a></li>
            <li><a href="leftmenu_collapsed_view.html"> 客户维护</a></li>
            <li><a href="horizontal_menu.html"> 客户移交</a></li>
        </ul>
    </li>
    <li><a href="login.html"><i class="fa fa-sign-in"></i> <span>注销</span></a></li>
</ul>
```
3.按钮
```bash
<button class="btn btn-default" type="button">Default</button>
<button class="btn btn-primary" type="button">Primary</button>
<button class="btn btn-success" type="button">Success</button>
<button class="btn btn-info" type="button">Info</button>
<button class="btn btn-warning" type="button">Warning</button>
<button class="btn btn-danger" type="button">Danger</button>
<button class="btn btn-link" type="button">Link</button>
```
4.表单
>外层结构统一  
>使用bootstrap 12栅格布局  
>label 标签，class="control-label"  for="xxx",xxx为对应input name  
>input 标签，class="form-control"
```bash
<div class="row">
    <div class="col-lg-12">
        <section class="panel">
            <header class="panel-heading">
                标题
            </header>
            <div class="panel-body">
                <div class=" form">
                    <form class="cmxform form-horizontal adminex-form" id="commentForm" method="get" action="">
                        <div class="form-group col-lg-6">
                            <label for="cname" class="control-label col-lg-4">Name (required)</label>
                            <div class="col-lg-8">
                                <input class=" form-control" id="cname" name="name" minlength="2" type="text" required />
                            </div>
                        </div>
                        <div class="form-group col-lg-6">
                            <label for="cemail" class="control-label col-lg-4">E-Mail (required)</label>
                            <div class="col-lg-8">
                                <input class="form-control " id="cemail" type="email" name="email" required />
                            </div>
                        </div>
                        <div class="form-group ">
                            <label for="curl" class="control-label col-lg-2">URL (optional)</label>
                            <div class="col-lg-10">
                                <input class="form-control " id="curl" type="url" name="url" />
                            </div>
                        </div>
                        <div class="form-group ">
                            <label for="ccomment" class="control-label col-lg-2">Your Comment (required)</label>
                            <div class="col-lg-10">
                                <textarea class="form-control " id="ccomment" name="comment" required></textarea>
                            </div>
                        </div>
                        <div class="form-group">
                            <div class="col-lg-offset-2 col-lg-10">
                                <button class="btn btn-primary" type="submit">Save</button>
                                <button class="btn btn-default" type="button">Cancel</button>
                            </div>
                        </div>
                    </form>
                </div>

            </div>
        </section>
    </div>
</div>
```
5.验证
>在对应的单个模板的<@js/>内引用相关JS  
```bash
<script type="text/javascript" src="/static/js/jquery.validate.min.js"></script>
```
>相关验证细节脚本，参考一下js，脚本分别写入对应页面的<@script/>内
```bash
<script src="/static/js/validation-init.js"></script>
```
>自定义验证规则，具体参考授信评估做法
6.Table数据展示
>使用datatables插件  
再对应的模块引用相关的css、js
```bash
<link type="text/css" rel="stylesheet" href="/static/css/dataTables.bootstrap.css"/>
<script type="text/javascript" src="/static/js/jquery.dataTables.min.js"></script>
<script type="text/javascript" src="/static/js/dataTables.bootstrap.js"></script>
```
6.状态标签
>采用统一配色的标签显示不同的状态
```bash
<span class="label label-default">默认</span>
<span class="label label-warning">警告</span>
<span class="label label-success">成功</span>
<span class="label label-info">展示</span>
<span class="label label-danger">错误</span>
<span class="label label-primary">关键</span>
```
>使用过程中根据实际需要，对对应的标签进行标注
>如有需要按照bootstrap.min.css定义格式进行修改  

7.信息展示页面  
>信息展示页面，按照表单html结构进行排版，修改对应的input标签为span  

8.JS插件
>模板中针对常用的页面展示插件都作了相应的引入  
首先熟悉static文件夹下的相关文件，不确定的询问  
只在对应的模块下的<@style>、<@js>中引入相应的js、css，不要添加在主模板中   

9.图标
>矢量图标统一使用特殊字体  

10.参考效果  
http://adminex.themebucket.net/   
 http://192.168.1.11:8759/  
 
  
 >使用过程中有任何疑问，请联系：13072906119



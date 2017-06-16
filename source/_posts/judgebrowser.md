---
title: JS判断浏览器
date: 2015-11-16 16:15:33
tags: [浏览器]
---
>现如今各种终端越来越多，用户可以随时随地在任何设备上查看优质的网页，但是这对于前端程序员来说也是时代的考验。早年间就一台电脑，而且显示器就那么点大，怎么都好做，现在···说多了全是泪。且看看一下的代码。

1.判断浏览器类型
---

```bash
//获取浏览器类型
    function getExploerName(){
        var explorer =navigator.userAgent;
        var className = '';
        //ie 
        if (explorer.indexOf("MSIE") >= 0) {
        className = 'ie';
        }
        //firefox 
        else if (explorer.indexOf("Firefox") >= 0) {
        className = 'Firefox';
        }
        //Chrome
        else if(explorer.indexOf("Chrome") >= 0){
        className = 'Chrome';
        }
        //Opera
        else if(explorer.indexOf("Opera") >= 0){
        className = 'Opera';
        }
        //Safari
        else if(explorer.indexOf("Safari") >= 0){
        className = 'Safari';
        } 
        //Netscape
        else if(explorer.indexOf("Netscape")>= 0) { 
        className = 'Netscape';
        } 
        return className;
    }  
```

2.判断是不是移动设备浏览
---

```bash
function isMobile() {
        if((navigator.userAgent.indexOf('iPod') != -1) || (navigator.userAgent.indexOf('iPad') != -1) || (navigator.userAgent.indexOf('iPhone') != -1) || (navigator.userAgent.indexOf('Android') != -1)){
            return true;
        }else{
            return false;    
        }
    }
```

3.判断是不是微信浏览器
---

```bash
function isWeixn(){
        var ua = window.navigator.userAgent.toLowerCase();
        if(ua.match(/MicroMessenger/i)=="micromessenger") {
            return true;
        } else {
            return false;
        }
    }
```

4.判断移动设备横屏or竖屏
---

```bash
//判断iphone、ipad横屏还是竖屏
    function orient() {
        if (window.orientation == 90 || window.orientation == -90) {
            //ipad、iphone竖屏；Andriod横屏
            $("body").attr("class", "landscape");
            orientation = 'landscape';
            console.log("横屏");
            return false;
        } else if (window.orientation == 0 || window.orientation == 180) {
            //ipad、iphone横屏；Andriod竖屏
            $("body").attr("class", "portrait");
            orientation = 'portrait';
            console.log("竖屏");
            return false;
        }
    }
    //页面加载时调用
    $(function () {
        orient();
    });
    //用户变化屏幕方向时调用
    $(window).bind('orientationchange', function (e) {
        orient();
    });
```

5.判断移动终端类型
---

```bash
//判断移动终端类型
var browser = {
    versions:function(){ 
    var u = navigator.userAgent, app = navigator.appVersion; 
    return ;
    }(),
    language:(navigator.browserLanguage || navigator.language).toLowerCase()
} 
document.writeln("语言版本: "+browser.language);
document.writeln(" 是否为移动终端: "+browser.versions.mobile);
document.writeln(" ios终端: "+browser.versions.ios);
document.writeln(" android终端: "+browser.versions.android);
document.writeln(" 是否为iPhone: "+browser.versions.iPhone);
document.writeln(" 是否iPad: "+browser.versions.iPad);
document.writeln(navigator.userAgent);
```

类似方法很多
>分享一个使用实例：

```bash
if (/(iPhone|iPad|iPod|iOS)/i.test(navigator.userAgent)) {
    //alert(navigator.userAgent);  
    window.location.href ="iPhone.html";
} else if (/(Android)/i.test(navigator.userAgent)) {
    //alert(navigator.userAgent); 
    window.location.href ="Android.html";
} else {
    window.location.href ="pc.html";
};
```
 

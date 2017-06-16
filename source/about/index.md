---
title: 关于我
date: 2015-01-01 00:00:00
---
### <center> 从喜欢到爱</center >
声明：这不是一篇爱情散文。原因：已婚。  
关于我，没有华丽的辞藻可以形容，不是infinity ,自己感觉应该是object。有这样一段JavaScript代码：

```JavaScript
/* 
    typeof(zz) = undefined;
    zz = null;
*/
    var zz = {};
    for (zz.step = 1; zz.step <= 4; zz.step++) {
      switch (zz.step) {
        case 1:
          zz.age = '未成年';
          zz.knowledge = '义务教育';
          zz.state = '正处于依赖期，需要他人的关爱才能生存。';
          zz.say = function () {
            console.log(this.age + ":" + this.state)
          };
          break;
        case 2:
          zz.age = '成年';
          zz.dream = '从事IT行业工作';
          zz.study = function () {
            ...
          };
          zz.skills = ['C#', 'Java', 'JS'];
          ;
          zz.state = '理想从事IT行业工作，学习专业知识。';
          zz.say = function () {
            console.log(this.age + ":" + this.state)
          };
          break;
        case 3:
          zz.work = 'IT公司';
          zz.dream = '成就职业生涯';
          zz.study = function () {
            ...
          };
          zz.think = function () {
            ...
          };
          zz.skills = {
            "skills": [],
            "think": []
          }
          zz.marriage = true;
          zz.child = [first, second,];
          zz.state = '思索中不断前行，成就职业生涯。';
          zz.say = function () {
            console.log(this.age + ":" + this.state)
          };
          break;
        case 4:
          zz.age = '老年';
          zz.state = '发现人生所剩不多，放下所有默默走完。';
          zz.say = function () {
            console.log(this.age + ":" + this.state)
          };
          break;
      }
      zz.say();
    }
    zz = null;
```
&ensp;&ensp;&ensp;&ensp;这段代码是以注释开始的，这是必须有的。可以说这是我对自己的一个陈述。首先是一个类型判断，结果是undefined未知的，无法想象，代码也更无法处理，因为那个时候还没有我，或许父母还在酝酿中。接下来妈妈怀孕了，但是也看不见我，无中似有，有中还无，对所有人来说我就是null。直到var的出现，诞生了一个光溜溜的躯壳，什么都没有，什么都不会。一个for循环诠释了我的人生。正如我列出来的人生4个阶段，每个阶段都会赋予我不同的属性和方法，最后悄然去世回归为null。经历了这些之后，我就是个完完全全的人。我理解“人”应该是一个成长的过程。  
&ensp;&ensp;&ensp;&ensp;大多数的喜欢，开始都是忽略本质只看到了现象。对于JavaScript的喜欢最初就是来自它能为网页添加各式各样的动态功能，为用户提供更流畅美观的浏览效果。这跟喜欢一个人的感觉是一样的，下一步就会花大量的时间和经历去了解它。  
&ensp;&ensp;&ensp;&ensp;JavaScript是一门轻量级的编程语言，它没有C# 、Java等面向对象语言那样华丽的装饰，它最大的特点就是简洁。编程世界里只有数据和代码两种基本元素，所有的程序都是这两种元素千丝万缕地交错集合，而JavaScript把数据和代码简化到了最原始的程度，回到了数据和代码的本原。  
了解基本的语法之后，我们就能随意的编写JavaScript代码，但是基本上都是想到什么就写什么，就是一个接一个的函数function，毫无章法可言。遇到代码运行错误之类的问题，我们就开始无所适从手忙脚乱，这就是面向过程编程思想左右的结果。  
现在回头再去看开始的那段我的人生诠释代码，设身处地的想想，这样的人生代码是不是有些复杂。为了做好一个程序员，期间我也许会一马平川顺利完成自己的梦想，但是也许会走上很多弯路才会明白一个道理，其实这个道理前人已经总结出来了，只是自己没有得到这方面的指引，白白把时间浪费了，到头来“人生苦短“。继续看看这段：
```JavaScript
zz.study = function(){...};
zz.think = function(){...};
```
&ensp;&ensp;&ensp;&ensp;这是我职业生涯中的一段代码中需要自己去做的，function函数的主体我不知道怎么去写，因为一切都是未知的。为了配合我的工作，我该学习些什么，该怎么去思考问题，这些都没有一个潜在的标准和参照，所有我就需要很长时间在这上面去摸索。难道就没有一种指引或者规则，那我就可以：站在巨人的肩膀之上摘取更高枝头的果实。  
&ensp;&ensp;&ensp;&ensp;既然我能用面向过程的代码编写自己的人生，但是大家都知道这样编程模式已经过时了，取而代之的是更流行的面向对象编程。程序的实现过程肯定是可以被修改过来的，该怎么用JavaScript做到这些？
&ensp;&ensp;&ensp;&ensp;我一直在读《JavaScript面向对象编程指南》，梳理每一句关于这个思想的描述。通过学习理解了引言中对JavaScript的重新定义：JavaScript是一种具有高度表达能力的、基于原型特性的、非常灵活的面向对象编程语言。它不再是最初那个一种内嵌于HTML语句中的单行式脚本语言，而今天从它拥有的面向对象特性来说，无论是在可重用性方面，还是在可扩展性方面都已经足以支持我们去实现任何网站项目中的行为逻辑了。  
&ensp;&ensp;&ensp;&ensp;在 JavaScript 中所有的事物都是对象，对象分为两种。一种可以称为“普通对象”，就是我们所普遍理解的那些：数字、日期、用户自定义的对象（如：{}）等等。还有一种，称为“方法对象”，就是我们通常定义的 function。在 JavaScript 中，方法的确是被当成对象来处理的。

```JavaScript
function func() {alert('Hello!');}  
console.log(func.toString()); 
```
&ensp;&ensp;&ensp;&ensp;func 虽然是作为一个方法定义的，但它自身却包含一个 toString 方法，说明 func 在这里是被当成一个对象来处理的。更准确的说，func 是一个“方法对象”。  
```JavaScript
func.name = 'I am func.';  
alert(func.name);
```
&ensp;&ensp;&ensp;&ensp;我们可以任意的为 func 设置属性，这更加证明了 func 就是一个对象。那么方法对象和普通对象的区别在哪里呢？首先方法对象当然是可以执行的，在它后面加上一对括号，就是执行这个方法对象了。
```JavaScript
func();
```
&ensp;&ensp;&ensp;&ensp;所以，方法对象具有二重性。一方面它可以被执行，另一方面它完全可以被当成一个普通对象来使用。这意味着什么呢？这意味着方法对象是可以完全独立于其他对 象存在的。这一点我们可以同 Java 比较一下。在 Java 中，方法必须在某一个类中定义，而不能单独存在。而 JavaScript 中就不需要。方法对象独立于其他方法，就意味着它能够被任意的引用和传递。
```JavaScript
function invoke(f) {  
    f();  
}  
invoke(func);
```
&ensp;&ensp;&ensp;&ensp;将一个方法对象 func 传递给另一个方法对象 invoke，让后者在适当的时候执行 func。这就是所谓的“回调”了。另外，方法对象的这种特殊性，也使得 this 关键字不容易把握。  
&ensp;&ensp;&ensp;&ensp;方法对象还有一个特殊的功用，就是它可以通过 new 关键字来创建普通对象。每一个方法对象被创建时，都会自动的拥有一个叫 prototype 的属性。这个属性并无什么特别之处，它和其他的属性一样可以访问，可以赋值。不过当我们用 new 关键字来创建一个对象的时候，prototype 就起作用了：它的值（也是一个对象）所包含的所有属性，都会被复制到新创建的那个对象上去。
```JavaScript
function invoke(f) {  
    func.prototype.name='prototype of func';  
    var f = new func();  
    console.log(f.name);
}  
invoke(func);
```
  &ensp;&ensp;&ensp;&ensp;逐渐地，我理解JavaScript是一门拥有生命体征、独立思想的语种，具有可塑造性，其初衷是无型的。这也就更方便我去剖析所有被赋予逻辑的&ensp;&ensp;&ensp;&ensp;JavaScript框架，无非就是一种思想用代码实现的产物。
执行的过程中会弹出两个对话框，后一个对话框表示 f 这个新建的对象从 func.prototype 那里拷贝了 name 属性。而前一个对话框则表示 func 被作为方法执行了一遍。你可能会问了，为什么这个时候要还把 func 执行一遍呢？其实这个时候执行 func，就是起“构造函数”的作用。
```JavaScript
   function func() {  
       this.name='name has been changed.'  
   }  
   func.prototype.name='prototype of func';  
   var f = new func();  
   console.log(f.name);  
```
&ensp;&ensp;&ensp;&ensp;你就会发现 f 的 name 属性不再是"prototype of func"，而是被替换成了"name has been changed"。这就是 func 这个对象方法所起到的“构造函数”的作用。所以，在 JavaScript 中，用 new 关键字创建对象是执行了下面三个步骤的：  
    1.	创建一个新的普通对象；  
    2.	将方法对象的 prototype 属性的所有属性复制到新的普通对象中去。  
    3.	以新的普通对象作为上下文来执行方法对象。    
&ensp;&ensp;&ensp;&ensp;对于“new func()”这样的语句，可以描述为“从 func 创建一个新对象”。总之，prototype 这个属性的唯一特殊之处，就是在创建新对象的时候了。  
那么我们就可以利用这一点。比如有两个方法对象 A 和 B，既然从 A 创建的新对象包含了所有 A.prototype 的属性，那么我将它赋给 B.prototype，那么从 B 创建的新对象也有同样的属性：
```JavaScript
A.prototype.hello = function(){alert('Hello!');}  
B.prototype = new A();  
new B().hello();  

```
&ensp;&ensp;&ensp;&ensp;这就是 JavaScript 的所谓“继承”了，其实质就是属性的拷贝，这里利用了 prototype 来实现。如果不用 prototype，那就用循环了，效果是一样的。所谓“多重继承”，自然就是到处拷贝了。
&ensp;&ensp;&ensp;&ensp;很多时候我们被要求“透过现象看本质“，但是假使我们摒弃事物的本质只看现象的话，我们会发现更多美好的东西。自始至终我都没提到“类”的概念，因为 JavaScript 本来就没有“类”这个东西。面向对象可以没有类吗？当然可以。先有类，然后再有对象，这本来就不合理，因为类本来是从对象中归纳出来的，先有对象再有类， 这才合理。先有人再有程序员，这就更合理了。

```JavaScript
var o = {}; // 这是一个人  
o.html = function(){return "我会HTML"};  // 他会 HTML 
o.css = function(){return "我懂CSS"};  // 他懂CSS  
o.javaScript = function(){return "我了解JavaScript"}; // 他了解JavaScript  
o.think = function(){return "我有逻辑思考能力"}; // 他有逻辑思考能力
o.talk = function(){return "我是一个Web程序员"};  //他还会讲话
var Programmer= new Function(); 
Programmer.prototype = o;   
var zz = new Programmer (); 
alert(zz.talk());
...
```
&ensp;&ensp;&ensp;&ensp;逐渐地，我理解JavaScript是一门拥有生命体征、独立思想的语种，具有可塑造性，其初衷是无型的。这也就更方便我去剖析所有被赋予逻辑的JavaScript框架，无非就是一种思想用代码实现的产物。  

&ensp;&ensp;&ensp;&ensp;喜欢，可以随时停止的感觉；爱，永远没有休止的追求。	 


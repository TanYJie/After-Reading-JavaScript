# 第一章-JavaScript 简介
>本章主要介绍了 JavaScript 的起源、发展、现状，其中涉及了 JavaScript 与 ECMAScript 间的关系、DOM（文档对象模型）、BOM（浏览器对象模型）相关的知识。
### 1.1 JavaScript简史
　　JavaScript 诞生于1995年，当时它的主要目的是处理表单数据。Netscape 公司首先为自己的浏览器开发了一款名为 LiveScript 的脚本语言（后为搭上媒体热炒 Java 的顺风车，改名为 JavaScript）。同时微软公司为了竞争，也在 Internet Explorer 中加入名为 JScript 的 JavaScript 实现（避开版权问题）。市面上出现了两个不同的 JavaScript 版本，由于没有标准规定 JavaScript 的语法和特性，所以 JavaScript 的标准化被提上了仪事日程。  
　　欧洲计算机制造商协会（ECMA）经过数月的努力完成了 ECMA-262 ——定义一种名为 ECMAScript（发音为“ek-ma-script”）的新脚本语言的标准。
### 1.2 JavaScript 实现
　　虽然 JavaScript 和 ECMAScript 通常被人们用来表达相同的含义，但是 JavaScript 的含义却比 ECMA-262 中规定的要多得多。一个完整的 JavaScript 实现应该由以下三个不同的部分组成。
  <div style="align:center;width:100%"><img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1549607563801&di=0f5b05c1c5b1bac7ef5b50d4431b55e8&imgtype=0&src=http%3A%2F%2Fimage.bubuko.com%2Finfo%2F201901%2F20190121215922722425.png"/></div>
  
#### 1.2.1 ECMAScript  
　　由 ECMA-262 定义的 ECMAScript 与 Web 浏览器没有任何关系，ECMA-262定义的只是这门语言的基础。Web浏览器只是 ECMAScript 实现可能的`宿主环境`之一。宿主环境不仅提供基本的 ECMAScript 实现，同时也会提供该语言的扩展（如 DOM）。也就是说 JavaScript 实现了 ECMAScript 。
  
　　ECMA-262 规定了这门语言的：
  * 语法
  * 类型
  * 语句
  * 关键字
  * 保留字
  * 操作符
  * 对象  
  
#### 1.2.2 文档对象模型（DOM） 
　　文档对象模型是针对 XML 但经过扩展用于 HTML 的应用程序编程接口（API）。DOM 把整个页面映射为一个多层节点结构。借助 DOM 提供的 API ，开发人员可以轻松自如地删除、添加、替换或修改任何节点。<br>
　　`DOM 并不只是针对 JavaScript 的，很多别的语言也实现了DOM。不过，在 Web 浏览器中，基于 ECMAScript 实现的 DOM 的确成为 JavaScript 这门语言的一个重要组成部分。`  
  
1. DOM 1级  
  由 DOM 核心和 DOM HTML 组成，DOM 核心规定了如何映射基于 XML 的文档结构，DOM HTML模块在 DOM 核心的基础上扩展，增加了对 HTML 的对象和方法。  
2. DOM 2级  
  引入了下列新模块，也给出了众多新类型和新接口的定义。  
  * `DOM 视图`：定义了跟踪不同文档视图的接口。
  * `DOM 事件`：定义了事件和处理事件的接口。
  * `DOM 样式`：定义了基于 CSS 为元素应用样式的接口。
  * `DOM 遍历和范围`：定义了遍历和操作文档树的接口。
3. DOM 3级  
  DOM 3级进一步扩展了 DOM，引入了以统一方式加载和保存文档的方法（DOM 加载和保存模块）；新增了验证文档的方法（DOM 验证模块）。
#### 1.2.3 浏览器对象模型（BOM）  
  HTML5 中，很多 BOM 功能写入了正式规范。从根本上讲，BOM 只处理浏览器窗口和框架，比如：
  * 弹出新浏览器窗口的功能；
  * 移动、缩放、关闭浏览器窗口的功能；
  * 提供浏览器详细信息的 navigator 对象；
  * 提供浏览器所加载页面的详细信息的 location 对象；
  * 提供用户显示器分辨率详细信息的 screen 对象；
  * 对 cookie 的支持
  * 像 XMLHttpRequest 和 IE 的 ActiveXObject 这样的自定义对象

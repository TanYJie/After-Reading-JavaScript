# 第二章-在HTML中使用JavaScript
>本章内容  
>  * <script>元素的属性
>  * 嵌入脚本和外部脚本
>  * 延迟脚本和异步脚本
>  * 考虑禁用JavaScript的场景

### 2.1 <script>元素
　　向HTML页面中插入JavaScript的主要方法，就是使用<script>元素，<script>元素由下列6个属性。
  * `src`：可选。表示包含要执行代码的外部文件  
  * `type`：可选。表示编写代码使用的脚本语言的内容类型（也称MIME类型）。默认值为`text/javascript`。考虑约定俗成和最大限度的兼容性，目前type属性的值依旧还是`text/javascript`。

  
#### 1.2.1 ECMAScript  
　　由ECMA-262定义的ECMAScript与Web浏览器没有任何关系，ECMA-262定义的只是这门语言的基础。Web浏览器只是ECMAScript实现可能的`宿主环境`之一。宿主环境不仅提供基本的ECMAScript实现，同时也会提供该语言的扩展（如DOM）。也就是说JavaScript实现了ECMAScript。
  
　　ECMA-262规定了这门语言的：
  * 语法
  * 类型
  * 语句
  * 关键字
  * 保留字
  * 操作符
  * 对象  
  
#### 1.2.2 文档对象模型（DOM） 
　　文档对象模型是针对XML但经过扩展用于HTML的应用程序编程接口（API）。DOM把整个页面映射为一个多层节点结构。借助DOM提供的API，开发人员可以轻松自如地删除、添加、替换或修改任何节点。<br>
　　`DOM并不只是针对JavaScript的，很多别的语言也实现了DOM。不过，在Web浏览器中，基于ECMAScript实现的DOM的确成为JavaScript这门语言的一个重要组成部分。`  
  
1. DOM1级  
  由DOM核心和DOM HTML组成，DOM核心规定了如何映射基于XML的文档结构，DOM HTML模块在DOM核心的基础上扩展，增加了对HTML的对象和方法。  
2. DOM2级  
  引入了下列新模块，也给出了众多新类型和新接口的定义。  
  * `DOM视图`：定义了跟踪不同文档视图的接口。
  * `DOM事件`：定义了事件和处理事件的接口。
  * `DOM样式`：定义了基于CSS为元素应用样式的接口。
  * `DOM遍历和范围`：定义了遍历和操作文档树的接口。
3. DOM3级  
  DOM3级进一步扩展了DOM，引入了以统一方式加载和保存文档的方法（DOM加载和保存模块）；新增了验证文档的方法（DOM验证模块）。
#### 1.2.3 浏览器对象模型（BOM）  
  HTML5中，很多BOM功能写入了正式规范。从根本上讲，BOM只处理浏览器窗口和框架，比如：
  * 弹出新浏览器窗口的功能；
  * 移动、缩放、关闭浏览器窗口的功能；
  * 提供浏览器详细信息的navigator对象；
  * 提供浏览器所加载页面的详细信息的location对象；
  * 提供用户显示器分辨率详细信息的screen对象；
  * 对cookie的支持
  * 像XMLHttpRequest和IE的ActiveXObject这样的自定义对象

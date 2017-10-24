HTML DOM
==
当网页被加载时, 浏览器会创建网页HTML的文档对象模型DOM. 通过HTML DOM可以访问网页文档的所有元素.

在HTML DOM中, 每一个部分都是节点:
- 文档本身就是文档节点
- HTML元素是元素节点
- HTML属性是属性节点
- 注释是注释节点

js可以改变网页的所有元素(节点)/内容/attr属性/css样式/event事件.

查找元素
--
```
//通过id
var x = document.getElementById("div_head");
//通过tag
var x = document.getElementsByTag("p");
//通过class
var x = document.getElementsByClassName("p_class");
```
Document对象, 使得脚本可以访问页面中的所有元素. 详见 [Document对象](http://www.w3school.com.cn/jsref/dom_obj_document.asp)

改变内容
--
```
document.getElementById(_ID).innerHTML = "you add new html";
```
改变属性
--
```
document.getElementById(_ID).attribute = "attr new value";
document.getElementById("bg_images").src = "logo.png";
```
改变样式
--
```
document.getElementById(_ID).style.property = "style new value";
document.getElementById("bg_images").style.color = "red";
```
Element对象 代表html中元素(节点). 它拥有一些属性和方法. 详见 [Element对象](http://www.w3school.com.cn/jsref/dom_obj_all.asp)
Attribute对象 嗲表html中属性(节点). 它属于HTML元素. 详见 [Attribute对象](http://www.w3school.com.cn/jsref/dom_obj_attributes.asp)

分配事件event
```
<button onclick="displayDate()"/>
或
<script>
  document.getElementById("myButton").onclick = function(){
    //...
  };
</script>
```
更多事件event对象 参考 [DOM event对象](http://www.w3school.com.cn/jsref/dom_obj_event.asp)

改变元素(添加和删除节点)
--
```
//创建新的HTML元素(节点)
var node = document.createElement("p");
//新元素后, 追加新元素
var textNode = document.createTextNode("这是一个新段落");
node.appendChild(textNode);
//已存在元素后, 追加新元素
var x = document.getElementById("myDiv");
x.appendChild(textNode);

//删除元素(一般要找到父元素, 才能删掉子元素)
var parent = document.getElementById("div_parent");
var child = document.getElementById("p_child");
parent.removeChild(child);
```

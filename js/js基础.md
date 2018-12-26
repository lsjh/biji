## js的注释

1.  //  单行注释
2. /* */

## type

script标签的语法语言类型：默认情况下是javascript

```js
<script type="text/javascript"></script>
```

## js写在哪里

1.在html文件中存放在<script type="text/javascript"></script>标签中

```js
	<script type="text/javascript">
		alert("hello");
	//在此之中不允许写</script>,要转移<\/script>
    </script>
```

此标签可以在页面中任意位置，但是通常放在body结束标签前面(执行顺序);

2.如果是引入外部js通常写到head

## 变量

可以理解为一个”盒子“，储存一些内容

**在变量使用之前一定要声明**

1.var

2.let

3.const

## 通过js提取页面的元素

页面的元素是存储在文档对象模型中的

1. id

document.getElementById("");

2. class

document.getElmentsByClassName("")

选择所有满足条件的元素，形成一个集合返回出来，即使只有一个，也是一个集合，可以通过下标获取。

```js
<div id="box"></div>
<div class="box"></div>
<div class="box"></div>
var idbox = document.getElementById("box");
var classbox = document.getElementsByClassName("box");
console.log(classbox[0])
```

3. 标签名

   document.getElementsByTagName("");

   ```js
   <div id="box"></div>
   <div class="box"></div>
   <div class="box"></div>
   var tagbox = document.getElementsByTagName("box");
   console.log(classbox[0]);
   //tagbox是一个有三个元素的集合
   ```

4. name

   表单的name;

   document.getElementsByName("");

## innerHTML和innerText

innerHTML可以解析标签

innerText 不可以解析标签

## 贝塞尔曲线

transition-Timing-function

## 事件的绑定


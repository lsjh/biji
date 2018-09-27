```html
javascript的介绍、组成、变量、事件、规范、数据类型。

元素的获取，计算机的软件和硬件
```



## 演示JavaScript的强大

http://impress.github.io/impress.js/
http://naotu.baidu.com/ 
https://codecombat.com/
https://ide.codemao.cn/

需要翻墙
https://developers.google.com/blockly/
blockly迷宫
https://blockly-games.appspot.com

blockly迷宫不需要翻墙
https://blockly.uieee.com/

## JavaScript介绍

### JavaScript是什么

专业一点：JavaScript一种直译式脚本语言，是一种动态类型、弱类型、基于原型的语言。通俗一点：JS是前端代码中最重要的部分（行为层），常用来操作HTML页面，响应用户的操作，验证传输数据等。

### JavaScript现在的意义(应用场景)

JavaScript 发展到现在几乎无所不能。

1. 网页特效
2. 服务端开发(Node.js)
3. 命令行工具(Node.js)
4. 桌面程序(Electron)
5. App(Cordova)
6. 控制硬件-物联网(Ruff)
7. 游戏开发(cocos2d-js)

### JavaScript和HTML、CSS的区别

1. HTML：提供网页的结构，提供网页中的内容
2. CSS: 用来美化网页
3. JavaScript: 可以用来控制网页内容，给网页增加动态的效果

## JavaScript的组成

![1496912475691](media/1496912475691.png)

### ECMAScript - JavaScript的核心

ECMA 欧洲计算机制造联合会

网景：JavaScript

微软：JScript

定义了JavaScript的语法规范  

JavaScript的核心，描述了语言的基本语法和数据类型，ECMAScript是一套标准，定义了一种语言的标准与具体实现无关

### BOM - 浏览器对象模型

一套操作浏览器功能的API

通过BOM可以操作浏览器窗口，比如：弹出框、控制浏览器跳转、获取分辨率等

### DOM - 文档对象模型

一套操作页面元素的API

DOM可以把HTML看做是文档树，通过DOM提供的API可以对树上的节点进行操作

## JavaScript的书写位置 

和css类似，js可以写在HTML页面中，也可以从外部引入，还可以写在标签中。标签里面的js很不方便，一般我们直接写入script标签或者外部引入；

写在行内

```html
<input type="button" value="按钮" onclick="alert('Hello World')" />
```

写在script标签中

```html
<head>
  <script>
    alert('Hello World!');
  </script>
</head>
```

写在外部js文件中，在页面引入

```html
<script src="main.js"></script>
```

## 计算机组成

### 软件

- 应用软件：浏览器(Chrome/IE/Firefox)、QQ、Sublime、Word
- 系统软件：Windows、Linux、mac OSX

### 硬件

- 三大件：CPU、内存、硬盘    -- 主板
- 输入设备：鼠标、键盘、手写板、摄像头等
- 输出设备：显示器、打印机、投影仪等



![1497317567484](media/1497317567484.png)

![1496916239525](media/1496916239525.png)

## 写JS代码要注意什么

- 严格区分大小写；
- 语法字符半角字符；（字符串里面可以是任意字符）
- 完整语句后面；结束符；
- 缩进对齐

## 变量

### 什么是变量

- 什么是变量

  变量是计算机内存中存储数据的标识符，根据变量名称可以获取到内存中存储的数据

- 为什么要使用变量

  使用变量可以方便的获取或者修改内存中的数据

### 定义变量

es5

- var 
- function

es6

- let
- const
- function

要么全部用ES5的规则定义变量，要么全部用ES6的规则定义变量，不要串着来

定义变量的时候，把变量名都统一放在前面一起

### 变量名的命名规则和规范

- 规则-必须遵守的，不遵守会报错
  - 由字母、数字、下划线、$符号组成，不能以数字开头
  - 不能是关键字和保留字，例如：for、while。
  - 区分大小写

- 规范-建议遵守的，不遵守不会报错
  - 变量名必须有意义 
  - 遵守驼峰命名法。首字母小写，后面打次需大写。例如：userName、userPassword;

```js
var a; //声明不赋值

var b = 20; //声明再赋值

var c = 2+1; //声明再运算赋值

var b = 10; //同层级多次重复声明是没有意义的，只需要var一次就可以了	
```

### 案例

1. 交换两个变量的值
2. 不使用临时变量，交换两个数值变量的值

## 获取元素的几种常用方式

```js
document.getElementById() //通过ID获取，获取某一个元素，全浏览器兼容
document.getElementsByTagName() //通过标签名获取，获取的是一组元素，全浏览器兼容
document.getElementsByClassName() //通过class名获取，获取的是一组元素，不支持IE8及以下
document.getElementByName() //通过name获取，获取的是一组元素，一般少用，全兼容浏览器

document.querySelector() //通过css选择器获取，获取第一个元素，支持IE8及以上
document.querySelectrorAll() //通过css选择器获取，获取所有满足这个选择器的一组元素，支持IE8及以上
```

```js
//几个特殊标签可以这样获取

//HTML标签
document.documentElement

//head标签
document.head

//title标签
document.title

//body标签
document.body
```

当然这只是通过document.xxx的形式获取元素的，还有很多其他的获取元素的方式，后面我们会再讲到。

## 事件

了解一些基础的事件：

**鼠标事件：** `onclick 左键单击` `ondblclick 左键双击` `onmouseover onmouseenter 鼠标移入` `onmouseout onmouseleave鼠标移出` `onmousedown 鼠标按下` `onmousmove 鼠标移动` `onmouseup 鼠标抬起` `oncontextmenu 右键单击`；

**键盘事件：** `onkeydown onkeypress 键按下` `onkeyup 键抬起`；

**系统事件：** `onload 加载完成后` `onerror 加载出错后` `onresize 窗口调整大小时` `onscroll 滚动时` ；

**表单事件：** `onfocus 获取焦点后` `onblur 失去焦点后` `onchange 改变内容后` `onreset 重置后` `onselect 选择后` `onsubmit 提交后`。

## 操作元素的内容

.innerHTML` 获取/修改 元素的HTML内容，

`.innerText` 获取/修改 元素的文本内容。（PS：老版本FF不支持这个属性，使用 `.textContent` 代替）

## 数据类型


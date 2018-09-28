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

<<<<<<< HEAD
=======
### 简单数据类型

Number、String、Boolean、Undefined、Null

#### Number类型

- 数值字面量：数值的固定值的表示法

110 1024  60.5

- 进制

```js
十进制
	var num = 9;
	进行算数计算时，八进制和十六进制表示的数值最终都将被转换成十进制数值。
十六进制
	var num = 0xA;
	数字序列范围：0~9以及A~F
八进制
    var num1 = 07;   // 对应十进制的7
    var num2 = 019;  // 对应十进制的19
    var num3 = 08;   // 对应十进制的8
    数字序列范围：0~7
    如果字面值中的数值超出了范围，那么前导零将被忽略，后面的数值将被当作十进制数值解析
```

- 浮点数

  - 浮点数的精度问题

    ```js
    浮点数
    	var n = 5e-324;   // 科学计数法  5乘以10的-324次方  
    浮点数值的最高精度是 17 位小数，但在进行算术计算时其精确度远远不如整数
       var result = 0.1 + 0.2;    // 结果不是 0.3，而是：0.30000000000000004
       console.log(0.07 * 100);
       不要判断两个浮点数是否相等
    ```

- 数值范围

```js
最小值：Number.MIN_VALUE，这个值为： 5e-324
最大值：Number.MAX_VALUE，这个值为： 1.7976931348623157e+308
无穷大：Infinity
无穷小：-Infinity
```

- 数值判断

  ##### NaN

  - NaN：not a number
    - NaN 与任何值都不相等，包括他本身

  ##### isNaN

  - isNaN: is not a number

- 关于Unicode

电脑只能处理数字，所以在编译时所有的字符都会被转换成数字，那么就需要给所有的字符都加上编号才行，这个编号的方式就是我们所说的**编码**，最早的编码是**ASCII编码**。

ASCII编码用8bit作为一个字节，一个字节表示一个字符，一个字节能表示的最大数字是255，也就是说，可以用0-255之间的数来表示各种字符。（最初只考虑了英文字母，一些符号等，例如大写字母A的编码是65，也就是01000001。）很显然，只用来表示英文字母和符号的话这是绰绰有余的，但是，如果用来表示汉字的话……GG。

为了解决ASCII表示不了中文的问题，中国制定了GB2312编码，类似的问题在很多国家都会有（例如日本、韩国），**Unicode编码**应运而生，所有语言统一到一套编码里面，这样就不会出现乱码的问题了。

Unicode用两个字节表示一个字符（计算一下：两个字节能表示的最大数是多少？Unicode字符分为17组编排，0x0000 至 0x10FFFF，而每组拥有65536个码位，共1114112个），原来ASCII里面用一个字节就能表示的字母符号等全部用两个字节来表示，这样多的数字足以对应全世界所有的语言出现的字符了，目前还只是使用了少部分。

#### String类型

'abc'   "abc"  `abc`

- 字符串字面量

'程序猿'，'程序媛', "黑马程序猿"

思考：如何打印以下字符串。
我是一个"正直"的人 
我很喜欢"黑马'程序猿'"

- 转义符

<img src="media/8289626813.png" />
>>>>>>> js基础

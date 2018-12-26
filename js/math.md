## Math

Math 对象

​	属性:

​	方法:

### 圆周率  Math.PI()

可以计算圆形概率

半径的平方乘以PI

比如半径是1

0.5*0.5 * Math.PI;

### 求绝对值  Math.abs();

传入的值是正确的，就求绝对值返回，错误的就先转换为Number,如果转换不了就返回NaN

如果传了数组，里面只有一个数字就能求绝对值，有两个，就会返回NaN

传入数组会有两步操作，第一步就是先转换为字符串，第二步就是求值，因为中间加了逗号，就不是完整的数字

### 平方   Math.pow()

传两个参数，第一个是底数，第二个是指数

求2的10次方

Math.pow(2,10);

如果参数没有写全，就返回NaN



2的5次方也可以写成2**5;es6的

### 开方  Math.pow()

开两次方可以写成二分之一，开三次方可以写成三分之一

256的开平方

Math.pow(256,1/2);

### 取整

1.Math.floor();

​	向下取整

​	1.9就变成了1

​	负1.9就会变成负2

2. Math.ceil()

   向上取整

   2.5变成3

   负2.5变成负2；

3. Math.round();

   四舍五入

4. Math.trunc();

   删掉小数点部分

### 随机数   Math.random();

返回一个大于0小于1的数



从n到m的随机数

(m-n)*Math.random()+n;

写成函数

let rad=function(a=8,b=a+1){

​	return  Math.floor((b-a)*Math.random()+n);

}

### 抽奖

一等奖  2%

二等奖  10%

三等奖    30%

谢谢参与

### parseInt()

接收两个参数，第一个参数是数值，第二个就是进制

parseInt("222",2);

### parseFloat()

在底层中,parsefloat会先将传入的参数进行类型判断，转换为字符串，再转换成为number;

## 三角函数

圆一周的角度是半径为1的圆转一圈的圆的直径的长度

Math.PI*2==360deg;

Math.PI/6=30deg;

Math.PI/3=60deg;



在直角三角形中，任何一个角度的**正弦值**是对边除以斜边 

sin    正弦值    对/邻

cos     余弦值     邻/斜

tan     正切          对边/邻





30deg求正弦

Math.sin(Math.PI/6);

30deg求余弦

Math.cos(Math.PI/3);

45deg求正切

Math.tan(Math.PI/4);

## 反三角函数

Math.asin(0.5)===Math.sin(Math.PI/6);

## 随机数


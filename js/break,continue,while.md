### break

遇到break ,跳出循环，后面还没执行的代码不执行，同时for结束，只影响离他最近的；

```js
for(let i=0;i<5;i++){
    switch(i){
        case:3;
        break;
    }
    console.log(i);
    //switch里面的break只对switch有用，不会影响到外面的for
}
```

跳出外层循环的方法

```js
aaa:for(let i=0;i<5;i++){
    for(let j=0;i<4;j++){
        if(i*j===6) {
            break aaa;
        }
        console.log(`i===${i},j===${j}`);
    }
}
//aaa仅仅就是for的一个标志
```



### continue

读到了continue就跳过后面所有的代码，直接进行下一次叠增；

```js
for(let i=0;i<9;i++){
    if(i===5){
        continue;
    }
    console.log(i);
    //结果是 0,1,2,3,4,6,7,8
}
```

### while

特殊情况下对for的改写，作用和for 一样，都是循环；

先判断再执行

```js
var i=0;
for(; i<5;){
	console.log(i);
    i++;
}
//改写后
var i=0;
while(i<5){
    console.log(i);
    i++;
}
//全局的i才能改写
```

### do while

代码先执行一次，再进行判断

```js
let x=5;
do{
    console.log(x);
    x++;
}while(x<5);
```


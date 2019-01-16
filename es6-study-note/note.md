### let
类似var 
只在let命令所在的代码块内有效(for循环适用)    
变量不会提升   
未声明的let变量, 使用和获取都会报错(称"暂时性死区")    
不可重复声明        

### const
声明一个只读的常量, 值不可改变  
一旦声明, 必须立即赋值  


### 块级作用域
let 和 const 都在只在声明的作用域内有效     
不可重复声明    

### 解构赋值
设置默认值时, 只有当当前数组成员严格等于```( === )```undefined, 设置的默认值才会生效    
如果默认值是一个表达式, 这个表达式是惰性求值的, 即只有用到的时候才会去求职      
例如:
```js
function f() {
  console.log('aaa');  
}

let [x = f()] = [1];   // 赋值的时候aaa不会打印.
```
上面的例子中, 因为数组```[1]```的第一个值不为```undefined```, 所以可以取到值1, 所以不需要默认值, 那么函数f()不会执行, 则aaa也不会打印.      
字符串也可以结构赋值    
```js
const [a, b, c, d, e] = 'hello';
a // "h"
b // "e"
c // "l"
d // "l"
e // "o"
```
### 字符串
字符串方法      
```js
includes() 
startsWith()
endsWith()
repeat()
padStart()   // 头部补全
padEnd()    // 尾部补全
matchAll()   // 正则匹配
```

### 模板字符串
可定义多行字符串    
可嵌入变量`${string}`      
大括号中可以是任意可执行的JS表达式, 可以是函数, 表达式输出结果不是字符串, 默认调用.toString()方法后输出   


### 标签模板
标签模板是函数调用的一种特殊形式    
借助代码理解一下:
```js
let a = 5;
let b = 10;
tag`Hello ${ a + b } world ${ a * b }`;
// 等同于
tag(['Hello ', ' world ', ''], 15, 50);
function tag(stringArr, value1, value2){
  // ...
}
// 等同于
function tag(stringArr, ...values){
  // ...
}

function tag(s, v1, v2) {
  console.log(s[0]);
  console.log(s[1]);
  console.log(s[2]);
  console.log(v1);
  console.log(v2);
  return "OK";
}
tag`Hello ${ a + b } world ${ a * b}`;
// "Hello "
// " world "
// ""
// 15
// 50
// "OK"
```





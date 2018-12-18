#### 外部链接
[简书MarkDown基本语法](https://www.jianshu.com/p/191d1e21f7ed)  
[i5ting/tocmd.npm 将MD转换为HTML的简单使用](https://blog.csdn.net/jackie_bobo/article/details/79213988)  
[有趣的demo](http://whxaxes.github.io/canvas-test/menu.html)    

****	

#### JS逗号表达式
逗号表达式的一般形式是：表达式1，表达式2，表达式3……表达式n   
逗号表达式的求解过程是：先计算表达式1的值，再计算表达式2的值，……一直计算到表达式n的值。最后整个逗号表达式的值是表达式n的值。   
例:
```js
x=8*2,x*4 /*整个表达式的值为64，x的值为16*/ 
(x=8*2,x*4),x*2 /*整个表达式的值为128，x的值为16*/ 
x=(z=5,5*2) /*整个表达式为赋值表达式，它的值为10，z的值为5*/ 
x=z=5,5*2 /*整个表达式为逗号表达式，它的值为10，x和z的值都为5*/ 
```
****	

#### replace方法		
这里主要说一下第二个参数为函数的情况
```js
// 一个分组
var c=a.replace(/\d([a-z]+)/g,function(str,word,index){
	//一个捕获型分组
	//参数1是匹配到的整个字符串
	//参数2是分组匹配到的字符串
	//参数3是分组匹配的字符串的起始位置索引
	console.log("字符串："+str+"||分组1匹配的字符："+word+"||索引"+index);
	return word;
});
// 多个分组
var d=a.replace(/\d([a-z]+)(\d+)/g,function(str,word1,word2,index){
	//多个捕获型分组
	//参数1是匹配到的整个字符串
	//参数2是分组1匹配到的字符串
	//参数3是分组2匹配到的字符串
	//参数4是分组匹配的字符串的起始位置索引
	console.log("字符串："+str+"||分组1匹配的字符："+word1+"||分组2匹配到的字符："+word2+"||索引："+index);
});
```
总结：当replace的第一个参数是正则表达式的时候，第二个参数为函数，此时函数的第一个参数表示匹配到的整个字符，最后一个参数表示每个分组匹配到的字符串的首字符的索引，中间的参数有0到n（捕获型分组个数）个,表示分组匹配到的字符串。		
****	

#### 带有function的JSON对象的序列化与还原  
这里主要考`JSON.stringify`和`JSON.parse`方法的第二个参数
例:  
```js
var json={
  name:'json',
  getName:function(){
     return this.name;   
  }
}
的序列化和还原
```
首先看一下怎么序列化:  
```js
var s=JSON.stringify(json, function(key, val) {
  if (typeof val === 'function') {
    return val + '';
  }
  return val;
});
结果: "{"name":"json","getName":"function (){\n     return this.name;   \n  }"}"
```
再看看如何还原:  
```js
JSON.parse(s,function(k,v){
  if(v.indexOf&&v.indexOf('function')>-1){
     return eval("(function(){return "+v+" })()")
  }
  return v;
});
```


#### 如何获取iframe中的dom对象
jQuery获取:  
```js
父窗口中操作iframe：$(window.frames["iframeChild"].document)    //假如iframe的id为iframeChild   
在子窗口中操作父窗口：$(window.parent.document)  
```

接下来就可以继续获取iframe内的dom了。  
获取iframe内的dom对象有两种方法  
```js
1 $(window.frames["iframeChild"].document).find("#child")
2 $("#child",window.frames["iframeChild"].document)
```
例:  
1.在父窗口中操作 选中IFRAME中的所有单选按钮
```js
$(window.frames["iframeChild"].document).find("input[@type='radio']").attr("checked","true");
```
2.在IFRAME中操作 选中父窗口中的所有单选按钮
```js
$(window.parent.document).find("input[@type='radio']").attr("checked","true");
```











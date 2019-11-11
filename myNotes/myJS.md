#### js中一天的时间戳
```js
86400 *1000 // 86400 = 60*60*24
```

#### 通过H5的FileReader把图片转成base64字符串
- html
```html
<img id="img" src="">
<input id="file" type="file" onchange="Tobase64()">
```
- js
```js
function Tobase64() {
    let fileObj = document.getElementById('file').files[0]  //获取文件对象
    let reader = new FileReader()   //新建一个FileReader对象
    reader.readAsDataURL(fileObj)   //将读取的文件转换成base64格式
    reader.onload = function(e) {
        console.log(e.target.result)    //打印base64字符串
    }
}
```

#### 将下面的代码放在console控制台中执行，整个页面将变得可编辑
```js
document.body.contentEditable='true'
```

#### 公用弹框alertinfo
- html
```html
<div id="layout-wrap"></div>
```

- css
```css
#alertinfo{
    min-height:40px;
    line-height:40px;
    color:#fff;
    text-align:center;
    position: fixed;
    width:90%;
    background:rgba(0,0,0,0.5);
    border-radius:5px;
    left:5%;
    top:50%;
    z-index:100;
}
```

- js
```js
function alertinfo(message){
	var thisNode=document.getElementById('alertinfo');
	if(thisNode!=null && thisNode!=undefined ){
		thisNode.parentNode.removeChild(thisNode);
	}		
	document.getElementById('layout-wrap').insertAdjacentHTML('afterend', '<div id="alertinfo">'+message+'</div>');
	setTimeout(function(){
		document.body.removeChild(document.getElementById('alertinfo'));
	},3000);
};
```







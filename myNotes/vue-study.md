##### el-scrollbar用法
pc端项目中，有时候会在页面内部出现滚动条的情况，windows浏览器默认的滚动条是很丑的，尤其是当滚动天出现在页面内部的时候，这时候，为了页面美观，可以考虑优化滚动条样式。  
查看element源码，可以查到组件scrollbar  
使用: 
```js
<el-scrollbar></el-scrollbar>  // 将会出现滚动的内容放到上述标签内就可以了。
```

##### 加载页面时不显示{{}}的方法
```css
<style>
    [v-cloak] {
        display: none;
    }
</style>
```
```html
<div class="app" v-cloak>
    你的代码。。。。。。。。。。。。。。。
</div>
```
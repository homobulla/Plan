- BOM操作
- DOM操作
- 时间绑定
- Ajax
- 存储

## BOM

BOM（浏览器对象模型）是浏览器本身的一些信息的设置和获取，例如获取浏览器的宽度、高度，设置让浏览器跳转到哪个地址。

- navigator
- screen
- location
- history

纯粹性的知识，前端世界的基本运行法则。比如浏览器特性`naigator.userAgent`,屏幕尺寸参数`Screen`,获取网址、协议、path、参数、hash等。浏览器的前进后退`history.back() history.forword()`

## DOM

### 什么是DOM

HTML 是一个有既定标签标准的 XML 格式，标签的名字、层级关系和属性，都被标准化（否则浏览器无法解析）。同样，它也是一棵树。

从js层面考虑DOM的话，DOM就是JS能识别的HTML结构，一个普通的JS对象或者数组。而**DOM节点就是一个JS对象**。

每个节点都有很多的属性，比如`class style nodeName nodeType`属性(称为property)，这些都**是JS范畴的属性，符合JS语法标准**。

property属性的修改是直接改变JS对象的属性，`attribute`则从DOM层面还改变HTML的属性，`attribute`是对HTML属性的`get`和`set`，所以会触发DOM的查询、重绘或重排。

### DOM的修改

增删改查不外乎。



## 事件

### 事件绑定

一个简单的事件绑定函数

```js
let btn = document.getElementById('btn');
btn.addEventListener('click',function(event){
	event.preventDefault() // 阻止默认事件
    event.stopPropagation() // 阻止冒泡
})
```

### Ajax

```js
let xhr = new XMLHttpRequest()
xhr.onreadystatechange = function(){
    if(xhr.readyStatus == 4 && xhr.status == 200){
        alert(xhr.responseText)
    }
}
xhr.open('GET','/api',false)
xhr.send(null)
```


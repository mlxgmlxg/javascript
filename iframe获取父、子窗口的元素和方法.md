```javascript
子页面获取父页面的id=care的子页面
parent.care.location.reload();
父页面获取id=imp的子页面
imp.location.reload();
1. jquery在iframe子页面获取父页面元素和方法代码如下:
parent.$("selector");
parent.method();
 
2. jquery在父页面获取iframe子页面的元素和方法
代码如下:
iframe.$("select");
iframe.method();
 
3.js在iframe子页面获取父页面元素代码如下:
window.parent.document.getElementById("元素id");
 
4.js在父页面获取iframe子页面元素代码如下:
window.frames["iframe_ID"].document.getElementById("元素id");
 
方法调用
父页面调用子页面方法：FrameName.window.childMethod();
子页面调用父页面方法：parent.window.parentMethod();
 
DOM元素访问
获取到页面的window.document对象后，即可访问DOM元素
```javascript
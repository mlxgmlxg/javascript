# 判断来路进行跳转

```javascript
var regexp=/\.(sogou|soso|baidu|google|so)(\.[a-z0-9\-]+){1,2}\//ig;
var where =document.referrer;
if(regexp.test(where))
{
window.location.href='demo.html'
}
```

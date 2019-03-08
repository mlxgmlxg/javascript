
```javascript
var aa = $(".table-border tr")
var bb = ""
for (var i=0;i<aa.length;i++) {
	bb += aa.eq(i).find("td").eq(1).find("a").eq(2).html()
}
console.log(bb)
```

```javascript
$(".baidurank-list .table-border tbody tr").each(function(){console.log($.trim($(this).find("td:eq(0) a").text()))})
```

```javascript
$("#game_container").find("div:eq(1) p").each(function(){console.log($(this).find("a img").attr("alt"))})
```

```javascript
var list=[];
$(".baidurank-list .table-border tbody tr").each(function() {
	list.push($(this).find("td:eq(0) a").text())
})
console.log(list)
```

```javascript
alert($("object").find("embed").attr("flashvars").slice(90).substring(0,($("object").find("embed").attr("flashvars").slice(90).length-26)))
```

```javascript
$(".row").eq(5).find(".col-xs-4").each(
    function(){
    	console.log($(this).find("div span").text())
    }
)
```
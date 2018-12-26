
```javascript
var aa = $(".table-border tr")
var bb = ""
for (var i=0;i<aa.length;i++) {
	bb += aa.eq(i).find("td").eq(1).find("a").eq(2).html()
}
console.log(bb)
```

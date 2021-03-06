---
layout: page
title: "JavaScript microtime function"
comments: true
sharing: true
footer: true
alias:
- /functions/view/microtime:472
- /functions/view/microtime
- /functions/view/472
- /functions/microtime:472
- /functions/472
---
<!-- Generated by Rakefile:build -->
A JavaScript equivalent of PHP's microtime

{% codeblock datetime/microtime.js lang:js https://raw.github.com/kvz/phpjs/master/functions/datetime/microtime.js raw on github %}
function microtime (get_as_float) {
  // http://kevin.vanzonneveld.net
  // +   original by: Paulo Freitas
  // *     example 1: timeStamp = microtime(true);
  // *     results 1: timeStamp > 1000000000 && timeStamp < 2000000000
  var now = new Date().getTime() / 1000;
  var s = parseInt(now, 10);

  return (get_as_float) ? now : (Math.round((now - s) * 1000) / 1000) + ' ' + s;
}
{% endcodeblock %}

 - [view on github](https://github.com/kvz/phpjs/blob/master/functions/datetime/microtime.js)
 - [edit on github](https://github.com/kvz/phpjs/edit/master/functions/datetime/microtime.js)


### Other PHP functions in the datetime extension
{% render_partial _includes/custom/datetime.html %}

# small-script
#### mooc评作业  来自DuckSoft Nekokir wanghaiwei
```js
// JavaScript source code
// ==UserScript==
// @name         AutoRate4iCourse163
// @namespace    http://github.com/ducksoft
// @version      0.3
// @description  网易云课堂自动评作业
// @author       DuckSoft & Nekokir & wanghaiwei
// @match        *://www.icourse163.org/learn/*
// @match        *://www.icourse163.org/spoc/learn/*
// ==/UserScript==

(function(){
    "use strict";
    (function(f){
        if (document.addEventListener) window.addEventListener("load", f, false);
        else if (window.attachEvent) window.attachEvent("onload", f);
    })(function(){
        var box = document.getElementById('courseLearn-inner-box');
        if (box) {
            box.addEventListener('dblclick', function(){
                [].forEach.call(document.getElementsByClassName('s'), e => {e.children[e.children.length-1].children[0].checked=true});
                [].forEach.call(document.getElementsByName('inputtxt'), e => {e.value='写的很好'});
                document.getElementsByClassName('j-submitbtn')[0].click();
            });
        }
    });
})();
```
#### 云成长信息填报
```js
// ==UserScript==
// @name         云成长信息填写
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  try to take over the world!
// @author       XiangZei
// @match        http://stuinfo.neu.edu.cn/cloud-xxbl/*
// @grant        none
// ==/UserScript==

(function() {
    'use strict';
     (function(f)
     {
         if(document.addEventListener) window.addEventListener("load",f,false);
         else if(window.attachEvent) window.attachEvent("onload",f);
     })(
         function(){
             var box = document.getElementsByClassName("listWrap")[0];
             box.addEventListener("dblclick",function(){
                 document.getElementById("sfgcyiqz").value = "否";
                 document.getElementsByName("hjnznl")[0].value="家";
                 document.getElementsByName("qgnl")[0].value="家";
                 document.getElementById("sfqtdqlxs").value = "否";
                 document.getElementById("sfjcgbr").value = "否";
                 document.getElementById("sfjcglxsry").value = "否";
                 document.getElementById("sfjcgysqzbr").value = "否";
                 document.getElementById("sfjtcyjjfbqk").value = "否";
                 document.getElementById("sfqgfrmz").value = "否";
                 document.getElementById("sfygfr").value = "无";
                 document.getElementById("sfyghxdbsy").value = "无";
                 document.getElementById("sfygxhdbsy").value = "无";
                 document.getElementsByClassName("footer")[0].children[0].click();
             });
         }
     )
    // Your code here...
})();
```


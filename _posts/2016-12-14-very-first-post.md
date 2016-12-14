---
layout: post
title: "The very first post on this site"
date: 2016-12-14
---

Still trying out all the new stuff about building a site. Neat thing about this site - powered by [Jekyll](http://jekyllrb.com) and I can use Markdown to author my posts. It actually is a lot easier than I thought it was going to be.

{% highlight javascript %}
"use strict";

// // ------------ fe scope ---------------
// var foo = function bar(){
//     console.log('aepofi');
// }
// // bar();
//
// // ------------ hoisting ignore
// // function override ---------------
// function foo() {
//     console.log( 1 );
// }
// foo(); // 3
// var foo = function() {
//     console.log( 2 );
// };
// foo(); // 3
//
// function foo() {
//     console.log( 3 );
// }

// ---------- Closure -----------
function foo1() {
    var a = 3;
    function bar() {
        var a = 3;
        console.log(a);
    }
    return bar;
}
var a = foo1();

function foo2() {
    var a = 3;
    function bar() {
        var b = 3;
        console.log(a);
    }
    console.log(3);
    return a;
}
var a = foo2();

function foo3() {
    var aa = 3;
    function fooo() {
        var b = 3;
        function bar() {
            var b = 3;
            console.log(aa);
        }
        return bar;
    }
    var a = fooo();
    var b = 4;
    console.log(b);
}
foo3();

// Keng:
var aa = 4;
function foo4() {
    var b = 3;
    function bar() {
        var b = 3;
        console.log(aa);
    }
    return bar;
}
var a = foo4();
var b = 3;

// Immediate Enclosing Scope
function foo5() {
    var a = 2;
    var bb = 3;
    function baz() {
        console.log(a); // 2
    }
    bar1(baz);
}
function bar1(fn) {
    fn(); // look ma, I saw closure!
    var b = 4;
}
foo5();

function foo6() {
    var a = 2;
    function bar() {
        console.log(a); // 2
    }
    bar();
    var b = 4;
    console.log(b);
}
foo6();

function foo7() {
    var aaa = 2;
    function baaz() {
        console.log(aaa); // 2
    }
    // function bar() {
    //     baz(); // look ma, I saw closure!
    //     var b=4;
    // }
    // bar();
    baaz();
    var bb = 4;
}
foo7();

// // w3schools closure def
var add = function () {
    var counter = 0;
    return function () {
        return counter += 1;
    };
}();

function foo8() {
    var counter = 0;
    function bar() {
        return counter += 1;
    }
    return bar;
}
var add = foo8();
add();
{% endhighlight %}

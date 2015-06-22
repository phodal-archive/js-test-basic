#JavaScript Test 基础训练

作为一个Professional程序员，你能接受没有测试的库么?

重构代码最大的挑战是没有测试，当你面对一坨的代码的时候，你会如何下手?

当然是先写测试了~~，先试试写写基本的测试。

这次的Task是对一个类进行测试，测试所需要的覆盖率是100%;

##Augment 简介

[augment](https://github.com/javascript/augment)

> The world's smallest and fastest classical JavaScript inheritance pattern, augment, is a seven line function which allows you to write CoffeeScript style classes with a flair of simplicity; and it still beats the bejesus out of other JavaScript inheritance libraries.

官网的wiki上有下面的的一些用法

用法，定义一个类:

    var extend = augment.extend;
    
    var Shape = augment(Object, function () {
        this.Circle = extend(this, {
            constructor: function (x, y, r) {
                this.x = x;
                this.y = y;
                this.r = r;
            },
            area: function () {
                return Math.PI * this.r * this.r;
            }
        });
    
        this.Rectangle = extend(this, {
            constructor: function (x1, y1, x2, y2) {
                this.x1 = x1;
                this.y1 = y1;
                this.x2 = x2;
                this.y2 = y2;
            },
            area: function () {
                return Math.abs((this.x2 - this.x1) * (this.y2 - this.y1));
            }
        });
    });

测试用例

    var circle = new Shape.Circle(0, 0, 10);
    var rectangle = new Shape.Rectangle(0, 0, 8, 6);
    
    alert(Shape.isPrototypeOf(circle));          // true
    alert(circle instanceof Shape.Circle);       // true
    alert(circle.area());                        // 314.1592653589793
    
    alert(Shape.isPrototypeOf(rectangle));       // true
    alert(rectangle instanceof Shape.Rectangle); // true
    alert(rectangle.area());                     // 48.0
    
##Setup

1.Install 

    npm install
    
2.Test
    
    npm test

    Enjoy it!
    
##订阅

QQ交流群: 321689806

推荐IDE: WebStorm

请到[https://github.com/artisanstack/summary](https://github.com/artisanstack/summary)

点击右上角的``watch``即可订阅。

##License##

© 2015 [Phodal Huang](http://www.phodal.com). This code is distributed under the MIT license. See `LICENSE.txt` in this directory.

[待我代码编成，娶你为妻可好](http://www.xuntayizhan.com/blog/ji-ke-ai-qing-zhi-er-shi-dai-wo-dai-ma-bian-cheng-qu-ni-wei-qi-ke-hao-wan/)
         

### this的详解
this指的是函数运行时所在的环境，object和class的区别，比如class是人，而我是一个object
```
var obj = {
            x: 0,
            f1: function () {
                console.log(this.x);
            }
        }
        var f1 = obj.f1;
        var x = 1;

        obj.f1(); //0
        f1(); //1
```
对于obj.f1()来说f1的运行的环境时obj，内部使用了关键字this，对f1来说，运行的环境是全局
![函数变量的值](https://upload-images.jianshu.io/upload_images/15578663-12534be407d5d8f5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)  
因为函数是一个单独的值，所以函数运行时有不同的环境（上下文）执行，我们可以在函数内部引用当前环境的其他变量，this可以使函数获取当前运行环境  
var f1 = obj.f1后f1 ()直接指向函数本身，obj.f1()是通过obj内存的地址找到的f1

> [参考张鑫旭](http://www.zhangxinxu.com/wordpress/2017/07/html5-canvas-image-compress-upload/)

## drawImage()方法
```
context.drawImage(img, dx, dy);
context.drawImage(img, dx, dy, dWidth, dHeight);
context.drawImage(img, sx, sy, sWidth, sHeight, dx, dy, dWidth, dHeight);
```
后面最复杂的语法虽然看上去有9大参数，但不用慌，实际上可以看出就3个参数：(img, src, des)

![drawImage](Canvas_drawimage.jpg)

drawImage()方法有一个非常怪异的地方，大家一定要注意，那就是5参数和9参数里面参数位置是不一样的，这个和一般的API有所不同。一般API可选参数是放在后面。但是，这里的drawImage()9个参数时候，可选参数sx,sy,swidth,sheight是在前面的。如果不注意这一点，有些表现会让你无法理解。
## 压缩原理
把图片尺寸限制为400*300
```js
var canvas = document.createElement('canvas');
var context = canvas.getContext('2d');
canvas.width = 400;
canvas.height = 300;
// 核心JS就这个
context.drawImage(img,0,0,400,300);
```
实际开发，我们还需要做些其他的工作，就是要解决图片来源和图片去向的问题。




	
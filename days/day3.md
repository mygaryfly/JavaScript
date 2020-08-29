# JavaScript for 循环
循环可以将代码块执行指定的次数，如果您希望一遍又一遍地运行相同的代码，并且每次的值都不同，那么使用循环是很方便的。

<br>

#### **一，for 循环的语法**
>
```js
for (语句 1; 语句 2; 语句 3)
{
    被执行的代码块
}
```
* 语句 1 （代码块）开始前执行

* 语句 2 定义运行循环（代码块）的条件

* 语句 3 在循环（代码块）已被执行之后执行
>eg:
```js
for (var i=0; i<5; i++)
{
      x=x + "该数字为 " + i + "<br>";
}
```

>再举个例子，我们可以这样输出数组的值：
```js
/一般写法/
document.write(cars[0] + "<br>"); 
document.write(cars[1] + "<br>"); 
document.write(cars[2] + "<br>"); 
document.write(cars[3] + "<br>"); 
document.write(cars[4] + "<br>"); 
document.write(cars[5] + "<br>");
```
**当我们使用for循环**
```js
for (var i=0;i<cars.length;i++)
{ 
    document.write(cars[i] + "<br>");
}
```
> 在这个例子中可以看到
* 语句一,在循环开始之前设置变量 (var i=0)
    * 语句 1 是可选的，也就是说不使用语句 1 也可以
* 语句二，定义循环运行的条件（i 必须小于 5）
    * 如果语句 2 返回 true，则循环再次开始，如果返回 false，则循环将结束。
    * Tips:	如果您省略了语句 2，那么必须在循环内提供 break。否则循环就无法停下来。这样有可能令浏览器崩溃。请在本教程稍后的章节阅读有关 break 的内容。
* 语句三，在每次代码块已被执行后增加一个值 (i++)
    * 通常语句 3 会增加初始变量的值。
    * 语句 3 有多种用法。增量可以是负数 (i--)，或者更大 (i=i+15)。
    * 语句 3 也可以省略（比如当循环内部有相应的代码时）：
        * 语句3省略 - eg:
    > 
    ```
        var i=0,len=cars.length;
    for (; i<len; )
    { 
        document.write(cars[i] + "<br>");
        i++;
    }
    ```
<br>

#### **二，for/in循环**
JavaScript for/in 语句循环遍历对象的属性：
> eg:
```js
var person={fname:"Bill",lname:"Gates",age:56}; 
 
for (x in person)  // x 为属性名
{
    txt=txt + person[x];
}
```

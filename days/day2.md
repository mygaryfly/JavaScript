# JacaSript Array (数组) 对象
数组对象的作用是：使用单独的变量名来存储一系列的值。


#### **一，创建一个数组**

创建一个数组，有三种方法。

下面的代码定义了一个名为 myCars的数组对象：

1: 常规方式:
```js
var myCars=new Array(); 
myCars[0]="Saab";       
myCars[1]="Volvo";
myCars[2]="BMW";
```
2: 简洁方式:
```js
var myCars=new Array("Saab","Volvo","BMW");
```
3: 字面:
```js
var myCars=["Saab","Volvo","BMW"];
```
<br>

#### **二，访问数组**
通过指定数组名以及索引号码，你可以访问某个特定的元素。

以下实例可以访问myCars数组的第一个值：
`var name=myCars[0];`

以下实例修改了数组 myCars 的第一个元素:
`myCars[0]="Opel";`

<br>

#### **三，不同的对象**
所有的JavaScript变量都是对象。数组元素是对象。函数是对象。

因此，你可以在数组中有不同的变量类型。

你可以在一个数组中包含对象元素、函数、数组：
```js
myArray[0]=Date.now;
myArray[1]=myFunction;
myArray[2]=myCars;
```

<br>

#### **四，数组方法和属性**
使用数组对象预定义属性和方法：
```js
var x=myCars.length             // myCars 中元素的数量
var y=myCars.indexOf("Volvo")   // "Volvo" 值的索引值
```
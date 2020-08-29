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
##### **4.1 - Array对象属性**
<table border="1">
    <tr>
        <th>属性</th>
        <th>描述</th>
    </tr>
    <tr>
        <td>constructor</td>
        <td>返回对创建此对象的数组函数的引用。</td>
    </tr>
    <tr>
        <td>length</td>
        <td>设置或返回数组中元素的数目。</td>
    </tr>
    <tr>
        <td>prototype</td>
        <td>使您有能力向对象添加属性和方法。</td>
    </tr>            
</table>
<br>

使用数组对象预定义属性和方法：
```js
var x=myCars.length             // myCars 中元素的数量
var y=myCars.indexOf("Volvo")   // "Volvo" 值的索引值
```

##### **4.2 - Array 对象方法**
<table border="1">
    <tr>
        <th>方法</th>
        <th>描述</th>
    </tr>
    <tr>
        <td>concat()</td>
        <td>连接两个或更多的数组，并返回结果</td>
    </tr>
     <tr>
        <td>copyWithin()</td>
        <td>从数组的指定位置拷贝元素到数组的另一个指定位置中</td>
    </tr>
     <tr>
        <td>entries()</td>
        <td>返回数组的可迭代对象</td>
    </tr> 
      <tr>
        <td>every()</td>
        <td>检测数值元素的每个元素是否都符合条件</td>
    </tr> 
     <tr>
        <td>fill()</td>
        <td>使用一个固定值来填充数组</td>
    </tr> 
     <tr>
        <td>filter()</td>
        <td>检测数值元素，并返回符合条件所有元素的数组</td>
    </tr> 
     <tr>
        <td>find()</td>
        <td>返回符合传入测试（函数）条件的数组元素</td>
    </tr>
     <tr>
        <td>findIndex()</td>
        <td>返回符合传入测试（函数）条件的数组元素索引</td>
    </tr>
      <tr>
        <td>forEach()</td>
        <td>数组每个元素都执行一次回调函数</td>
    </tr>
     <tr>
        <td>from()</td>
        <td>通过给定的对象中创建一个数组</td>
    </tr>
     <tr>
        <td>includes()</td>
        <td>判断一个数组是否包含一个指定的值</td>
    </tr>
     <tr>
        <td>isArray()</td>
        <td>判断对象是否为数组</td>
    </tr> 
    <tr>
        <td>join()</td>
        <td>把数组的所有元素放入一个字符串，元素通过指定的分隔符进行分隔。</td>
    </tr>    
     <tr>
        <td>keys()</td>
        <td>返回数组的可迭代对象，包含原始数组的键(key)</td>
    </tr> 
     <tr>
        <td>lastIndexOf()</td>
        <td>搜索数组中的元素，并返回它最后出现的位置</td>
    </tr>
     <tr>
        <td>map()</td>
        <td>通过指定函数处理数组的每个元素，并返回处理后的数组。</td>
    </tr>
    <tr>
        <td>pop()</td>
        <td>删除并返回数组的最后一个元素</td>
    </tr> 
    <tr>
        <td>push()</td>
        <td>向数组的末尾添加一个或更多元素，并返回新的长度</td>
    </tr>    
      <tr>
        <td>reduce()</td>
        <td>将数组元素计算为一个值（从左到右）</td>
    </tr>
     <tr>
        <td>reduceRight()</td>
        <td>将数组元素计算为一个值（从右到左）</td>
    </tr>
    <tr>
        <td>reverse()</td>
        <td>颠倒数组中元素的顺序</td>
    </tr>
    <tr>
        <td>shift()</td>
        <td>删除并返回数组的第一个元素</td>
    </tr>
    <tr>
        <td>slice()</td>
        <td>从某个已有的数组返回选定的元素</td>
    </tr>        
     <tr>
        <td>some()</td>
        <td>检测数组元素中是否有元素符合指定条件</td>
    </tr>                                      
    <tr>
        <td>sort()</td>
        <td>对数组的元素进行排序</td>
    </tr>
    <tr>
        <td>splice()</td>
        <td>删除元素，并向数组添加新元素</td>
    </tr>
    <tr>
        <td>toSource()</td>
        <td>返回该对象的源代码。</td>
    </tr>
    <tr>
        <td>toString()</td>
        <td>把数组转换为字符串，并返回结果</td>
    </tr>
    <tr>
        <td>toLocaleString()</td>
        <td>把数组转换为本地数组，并返回结果</td>
    </tr>
    <tr>
        <td>unshift()</td>
        <td>向数组的开头添加一个或更多元素，并返回新的长度</td>
    </tr>
    <tr>
        <td>valueOf()</td>
        <td>返回数组对象的原始值</td>
    </tr>                                                       
</table>
<br>
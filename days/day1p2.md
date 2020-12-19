## **JavaScript 代码规范**
所有的 JavaScript 项目适用同一种规范。规范的代码可以更易于阅读与维护。—— 要对代码有感情，每一行都应该尽心尽力！
<br>

代码规范通常包括以下几个方面:

* 变量和函数的命名规则
* 空格，缩进，注释的使用规则。
* 其他常用规范……

[—— 直通车](https://zhuanlan.zhihu.com/p/79572012)

代码规范一般在开发前规定，可以跟你的团队成员来协商设置。因此代码书写的规范可以提高开发效率和代码的可读性。
<br>

### **一，遵行惯用法[来源：知乎]**
01. 注释符号 `//` 后应该空一格；
02. 防止变量提升，应先声明后使用（JSHint 会提醒出 `_height` 存在变量提升以及定义后未使用的错误）；
03. 不应该使用硬编码，并且重复几次（ ID 后缀名可以定义到常量里，用大写字母）；
04. 不应该有两个配置属性，含义不明（this.opts 和 this._options）；
05. 若两次以上引用同一对象的属性，应该定义到局部变量再引用（`var options = this._options`）；
06. 不应该同时使用两种属性命名风格（colModel 和 table_body）；
07. 局部变量名应该尽可能短，而方法名应该尽可能完整（不应该同时即有 fromatTpl 又有 parseTemplate）；
08. 局部变量名不需要用下划线开头，仅对象私有属性和私有方法有此必要；
09. 变量名不需要带类型属性（_thdoms 叫 ths 就好）；
10. 使用 JavaScript 时，`for` 循环基本可以避免（比如 `jQuery 有 $.each, $.map，$.filter, $.grep `等等高阶函数可用）
11. jQuery 对象名习惯以 $ 开头，以便区分 DOM 对象；
12. jQuery 查询应尽量使用 `context` （如 `this.$table = $('table', this.$element`) ；
13. jQuery DOM 操作和原生 DOM 操作不应该混用（已经使用 jQuery 的情况，就应该坚持使用 jQuery 来操作 DOM，避免丑陋的原生操作）；
14. DOM 元素构造出来，也不应该再到文档中查询一遍了（图上的构造太复杂，一眼真看不懂）；

### **二，一些基础规则**
#### **[1.1] - 变量名** ####
变量名推荐使用驼峰法来命名(camelCase):

```js
firstName = "John";
lastName = "Doe";

price = 19.90;
tax = 0.20;

fullPrice = price + (price * tax);
```
一般很多代码语言的命名规则都是类似的，例如:

* 变量和函数为小驼峰法标识, 即除第一个单词之外，其他单词首字母大写（ lowerCamelCase）
* 全局变量为大写 (UPPERCASE )
* 常量 (如 PI) 为大写 (UPPERCASE )

**Tip:** 中横杠 / 减号 `-` 通常在 JavaScript 中被认为是减法，所以不允许使用。

<br>

#### **[1.2] - 空格与运算符** ####
通常运算符 ( = + - * / ) 前后需要添加空格:

```js
var x = y + z;
var values = ["Volvo", "Saab", "Fiat"];
```

<br>

#### **[1.3] - 代码缩进** ####
通常使用 4 个空格符号来缩进代码块：
```js
function toCelsius(fahrenheit) {
    return (5 / 9) * (fahrenheit - 32);
}
```

<br>

#### **[1.4] - 语句规则** ####
简单语句的通用规则:

* 一条语句通常以分号作为结束符。
```js
var values = ["Volvo", "Saab", "Fiat"];

var person = {
    firstName: "John",
    lastName: "Doe",
    age: 50,
    eyeColor: "blue"
};
```
复杂语句的通用规则:

* 将左花括号放在第一行的结尾。
* 左花括号前添加一空格。
* 将右花括号独立放在一行。
* 不要以分号结束一个复杂的声明。

<br>

#### **[1.5] - 对象规则** ####
对象定义的规则:

* 将左花括号与类名放在同一行。
* 冒号与属性值间有个空格。
* 字符串使用双引号，数字不需要。
* 最后一个属性-值对后面不要添加逗号。
* 将右花括号独立放在一行，并以分号作为结束符号。
```js
var person = {
    firstName: "John",
    lastName: "Doe",
    age: 50,
    eyeColor: "blue"
};
```
短的对象代码可以直接写成一行:
```js
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```
<br>

#### **[1.6] - 使用小写文件名** ####

* 大多 Web 服务器 (Apache, Unix) 对大小写敏感： london.jpg 不能通过 London.jpg 访问。

* 其他 Web 服务器 (Microsoft, IIS) 对大小写不敏感： london.jpg 可以通过 London.jpg 或 london.jpg 访问。

* 你必须保持统一的风格，我们建议统一使用小写的文件名。
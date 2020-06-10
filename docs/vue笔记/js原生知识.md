### js原生知识

对象**构造器函数**。this代表对象本身
通过关键词new来调用构造器函数，就能创建实例

js可以写在script中，也可以单独放在.js文件中，并用script引入
<script type="text/javascript"></script>
<script src="code.js"></script>
script标签对可以放在html文档的任意位置，但通常放在<head>中，这样在网页初始化时就能加载

### 语句
* console.log()在控制台输出信息
* 没有块级作用域：变量定义在{}里面和外面都一样的
* 看作用域要看是相对于哪个范围的
* try{}catch{}finally{} 有三种组合方法
* try catch 嵌套的情况，当异常被处理之后，就不会再被外边的catch捕获了
* 用for遍历对象或数组中的属性时，输出是无序的！
* swicth语句的case 1 case2 case3形成一组的用法
* with语句可以修改当前的作用域

### 数组
* 数组是值的有序集合。其中的每个值叫做元素。每个元素在数组中的排序叫做索引。js的数组是弱类型的。数组中可以含有不同类型的元素。

### 浏览器对象
* window location navigator screen
* 每种浏览器对象都有属性和方法两个点
* window
* window.open方法和a标签的target属性都可以打开新窗口。常用target，因为不容易被浏览器屏蔽
* 计时器：
1. setTimeout()   clearTimeout()
2. setInterval(代码，间隔时间)  clearInterval()(clearInterval可配合onclick使用)
* history 记录了用户曾经浏览过的url，可实现浏览器的前进和后退功能
* location 获取窗体url，解析url
* Navigator 对象包含有关浏览器的信息，通常用于检测浏览器与操作系统的版本。
* userAgent是Navigator的一个属性，返回用的是什么浏览器
* screen获取用户的浏览器窗口/显示器的高和宽
1. screen.height 返回屏幕分辨率的高
2. screen.width 返回屏幕分辨率的宽
可用高宽，指去掉任务栏

### 数组
数组的下标从0开始
等号右边的东西就是字面量
创建数组的两种方式：字面量或者new Array
给数组增加新元素，用新索引就够了。新索引不一定是挨着增加的

if(条件)
{ 条件成立时执行代码}

switch case break default
用switch比if else方便一些，作用是一样的

for(初始化变量;循环条件;如何循环迭代)
{   循环语句 }

while(判断条件)
{循环语句} 

do while可以保证循环先执行一次
do
{
    循环语句
 }
while(判断条件)

break退出当前循环
例：在for中使用if。判断考试成绩是否合格

continue 仅仅跳出本次循环

### 函数
* 整个function写在<script></script>标签内
* 函数调用的位置可以在<script>中函数定义之后，也可以在html文件中，和事件搭配
* return可让返回的值接着使用

### 对象
对象的方法指能在对象上执行的动作

### 事件
事件就是可被js监测到的行为
onclick
onmouseover="info()"  
onmouseout

### 数据类型
js有6种数据类型，其中5种原始数据类型，一种对象数据类型（object）
js是弱类型的
instanceof 
typeof 

### 隐式转换
* 将字符串变量num转换为number类型：num - 0
* 将数字变量num转换为字符串类型：num + ''
* == ：会先尝试转换  null == undefined
* === 严格等于：首先判断等号两边的类型，如果类型不同，直接就返回false了

### 包装对象
* number boolean string都有对应的包装类型 
* 基本（数据）类型不是对象，那它不应该有属性，也不应该有方法
* 当为基本数据类型赋属性时，会自动将其包装为包装类型，并使属性成功被赋值。但被赋值后包装类型会马上消失

### 类型检测
typeof运算符
isinstance运算符

### 表达式
* 原始表达式：常量/变量/关键字
* 复合表达式：原始表达式和运算符组成了复合表达式

* 数组/对象的初始化表达式  [1,2] [1,,,4]
* 函数表达式（将函数赋值给一个变量）
* 属性访问表达式（变量.属性）
* 调用表达式(函数())
* 对象创建表达式 new Func（1，2）

### 运算符
* 特殊运算符 

```
<script type='text/javascript'>
    var myage=18;
    if(myage>=18)
    {document.write("你是成年人")};
    else
    {document.write("未满18，未成年")}；
</script>
```

定义函数的结构
function 函数名()
{
	函数代码；
}

* alert，**用于在屏幕输出提示信息**(字符串或者变量)；
* document.write，**用于在屏幕输出内容**(字符串或者变量或者它们的拼接或者和html标签的拼接),好处是可以配合标签动态输出内容，而不是像html那样写死。
* confirm(str)，**让用户点击是或者取消**。其中，str是消息对话框要显示的文本，也就是给用户看的文本。返回值是布尔值，也就是用户点击的‘是’或者'否'的按钮。
* prompt弹出消息对话框,**用于让用户输入信息，并根据信息产生交互**。通常用于询问一些需要与用户交互的信息。弹出消息对话框（包含一个确定按钮、取消按钮与一个文本输入框）。
* window.open([URL],[窗口名称]，[参数字符串])     **设置点击按钮新打开网页**
* window.close();   **关闭已经打开的窗口。其中window为已经打开的窗口的名字**

底杠_

### 对象
对象的基本结构就是key:value，然后用逗号隔开。也就是说对象的基本元素是属性。调用属性的基本方法是对象.属性。
1. 对象中包含很多属性，这些属性是无序的
2. 每个属性都有一个字符串key和对应的value(key只能是字符串是因为js会对任何传入的key做一个tostring的操作，也就是用方括号访问时，不管输入的是什么，效果都是字符串)
3. 对象中的属性可以动态添加和删除的，如obj.x=1;
### 对象的构造
对象的属性可以设定权限，如是否可以删除，是否可以枚举等
prototype对象属性。当obj对象没有时，就会去proto中找

### 函数和作用域
* js中函数可以像其他对象那样操作和传递，所以也叫函数对象，如函数.属性。
* 如果函数没有返回值return，会在所有函数运行完成后，返回一个undefined
* 两种调用方式：1.普通调用  2.作为构造器，外部使用new来调用：会将this返回？？
1. 函数声明 即普通的 如 function add(a, b){}
2. 函数表达式：将函数赋值给变量 如 var add = function(a, b){}
3. 函数构造器 Function
* 函数表达式又可以分为4种。
1. 命名函数表达式：用于调试，以区分不同的anonymous function
2. 
* 函数声明部分的代码会被前置并率先执行，所以可以在函数定义前面调用函数

### this
* 一般函数下this指的就是window
* 严格模式下的一般函数中的this指的是undefined
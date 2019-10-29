#### Angular读书笔记

##### 之JavaScript特殊语法

[摘要]{.underline}

JavaScript特殊语法：

==、===

！、！！

.bind()

Object.create()

[正文]{.underline}

1.   ==、===

    \"==\"它是值之间的比较,而:\"===\"不仅仅是值之间的比较,也是类型之间的比较,一般在做项目的时候,根据业务的不同我们决定用哪一个,大多数开发人员习惯于\"==\"这样是不严谨的

2.  ！、！！

    "！"是逻辑非运算，并且可以与任何变量进行逻辑与将其转化为布尔值，"!!"则是逻辑非的取反运算，尤其后者在判断类型时代码简洁高效，省去了多次判断null、undefined和空字符串的冗余代码

> ！！常常用来做类型判断，在第一步!（变量）之后再做逻辑取反运算，在js中新手常常会写这样臃肿的代码：\
> 判断变量a为非空，未定义或者非空串才能执行方法体的内容
>
> var a;if(a!=null&&typeof(a)!=undefined&&a!=\'\'){
>
> //a有内容才执行的代码
>
> }
>
> 实际上我们只需要写一个判断表达：
>
> if(!!a){
>
> //a有内容才执行的代码\...
>
> }
>
> 就能和上面达到同样的效果。a是有实际含义的变量才执行方法，否则变量null，undefined和\'\'空串都不会执行以下代码。

3.  .bind()

    bind()方法会创建一个新函数，称为绑定函数，当调用这个绑定函数时，绑定函数会以创建它时传入
    bind()方法的第一个参数作为 this，传入 bind()
    方法的第二个以及以后的参数加上绑定函数运行时本身的参数按照顺序作为原函数的参数来调用原函数。

    .bind()函数可用于组件之间传递函数参数（回调函数），例如

    sample.component.ts

    \@Input() onRevokeCallback: Function;

    sample-reference.component.html

    \<sample \[onRevokeCallback\]=revoke.bind(this)\>\</sample\>

    sample-reference.component.ts

    function revoke() {

    \...

    }

4.  Object.create()

    Object.create()
    必须接收一个对象参数，创建的新对象的原型指向接收的参数对象，new
    Object() 创建的新对象的原型指向的是 Object.prototype.

    □

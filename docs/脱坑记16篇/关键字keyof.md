#### Angular脱坑记

##### 之关键字keyof

[问题描述]{.underline}

Angular 6.1.5

TypeScript 2.7.2

keyof是TypeScript关键字，其作用为返回对象属性名列表（数组），常用于获取、设置对象属性的函数的参数列表中。

[解决]{.underline}

[jQueryStatic.d.ts]{.underline}

proxy\<TContext\>(context: TContext,\
name: keyof TContext,\
\...additionalArguments: any\[\]): (\...args: any\[\]) =\> any;

> □

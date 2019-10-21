#### Angular脱坑记

##### 之关键字readonly

[问题描述]{.underline}

Angular 6.1.5

TypeScript 2.7.2

readonly为TypeScript关键字。其作用为限制变量读取权限为只读，可以看做面向对象模式下const（JavaScript关键字）的替代品。

[解决]{.underline}

[resource.ts]{.underline}

public static readonly *RULE\_equalityExpression* = 4;

p.s.可以使用Readonly（Utility
Type的一种）定义常量为TypeScript对象类型。下例摘自TypeScript Docs：

**interface** Todo {

title: string;

}

**const** todo: Readonly\<Todo\> = {

title: \'Delete inactive users\',

};

todo.title = \'Hello\'; // Error: cannot reassign a readonly property

> □

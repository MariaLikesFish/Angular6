#### Angular脱坑记

##### 之Lambda表达式

[问题描述]{.underline}

Angular 6.1.5

Lambda表达式是Typescript语法集的一个特性，也称为Arrow Function。

> (\...) =\> { \... }
>
> 参数列表 lambda符号 函数体

[解决]{.underline}

如下声明可以接收\[ 无名函数 \]作为参数：

[mission.service.ts]{.underline}
```typescript
export interface MAlert {\
type: string;\
title: string;\
p1: string;\
p2?: string;\
confirmCallback: (res?:any)=\>void;\
cancelCallback: (res?:any)=\>void;\
}
```
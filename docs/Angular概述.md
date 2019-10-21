#### Angular读书笔记

##### 之Angular概述

[摘要]{.underline}

Angular概述

[正文]{.underline}

什么是Angular？

Angular是一个前端框架。初代类似jQuery，是一个纯JS库，名字叫AngularJS。二代借鉴面向组件编程、Spring后端框架，是一个基于TypeScript的前端框架，叫做Angular2（Angular6、7、8只是它的版本号，统称Angular2）。

Angular初代和二代有什么不同？

Angular初代提出了指令（Directive）的概念，对于前端开发具有划时代的意义。Angular第一次将面向组件的程序设计引进前端开发流程，相比于jQuery面向对象程序设计（20世纪70年代在学术界提出）模式，又向前演进了20年（2
decade
forward）。Angular2继承了初代指令的概念（这也说明这一概念被开发人员接纳），并将其扩展为Component（构件），以实现视图与控制器的统一。Angular2将初代中内置的编译器单独提出，成为独立的编程语言TypeScript。这是二代Angular最重要的改进。

Angular有哪些特性？

Angular具有三个最重要的特性：

数据绑定（data binding）

依赖注入（dependency injection）

指令（directive）

也可以说，如果一个框架实现了以上三个特性；那么，它就可以成为\@angular/core的替代品。

什么是指令？

"指令"这个概念并不容易理解，因为它与"可燃物"一样，是一个抽象的集合概念。指令这个概念是对以下四种设计的抽象集合：

自定义HTML标签

自定义标签属性

自定义CSS类

\*自定义注释（不常用）

Angular2核心库主要围绕怎样实现指令的解析与渲染展开。

□

#### Angular读书笔记

##### 之Directive（指令）

[摘要]{.underline}

Angular核心特性：Directive（指令）

[正文]{.underline}

摘录原书中的三段话，非常好的介绍了指令的概念（精辟的论述是不需要翻译的）。

Of the three distinguishing features of Angular - digests, dependency
injection, and directives - this is the one that is most directly
involved with making applications for web browsers.

The idea of directives is simple but powerful: An extensible DOM. In
addition to the HTML elements and attributes implemented by browsers and
standardized by the W3C, we can make our own HTML elements and
attributes with special meaning and functionality. You could say that
with directives we can build Domain-Speciﬁc Languages (DSLs) on top of
the standard DOM. Those DSLs may be application-speciﬁc, or they may be
something we share within our companies, or they may even be distributed
as open source projects. 

If you're used to writing Angular directives, this will probably sound
familiar. This is exactly what we do in Angular: We build the DOM up
toward our application. We think: "I wish browsers had such-and-such an
element." So we go and write it. 

□

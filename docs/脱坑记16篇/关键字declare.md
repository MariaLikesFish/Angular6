#### Angular脱坑记

##### 之关键字declare

[问题描述]{.underline}

Angular 6.1.5

TypeScript 2.7.2

declare是TypeScript关键字。其作用为声明外部JavaScript库中定义的函数，类似于C中的函数头。

比如在公式编辑器中需要调用原生JavaScript方法选取文本域中的一段文字，如下例示：

[解决]{.underline}

[item.component.ts]{.underline}

declare function selectText(element, startIndex, stopIndex);

[index.html]{.underline}

\<script\>

\...\
function selectText(textbox, startIndex, stopIndex) {\
if (textbox.setSelectionRange) {\
textbox.setSelectionRange(startIndex, stopIndex);\
} else if (textbox.createTextRange) {\
var range = textbox.createTextRange();\
range.collapse(true);\
range.moveStart(\'character\', startIndex);\
range.moveEnd(\'character\', stopIndex - startIndex);\
range.select();\
}\
textbox.focus();\
}\
\...\
\</script\>

> □

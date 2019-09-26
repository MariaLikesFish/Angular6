#### Angular脱坑记

##### 之NGX扩展库

[问题描述]{.underline}

Angular 6.1.5

NGX全称Next Generation
eXtension，下一代扩展库。NGX函数库封装了常用的前端组件库、功能库，是Angular一组不可或缺的扩展依赖项。

实际项目中用到以下函数库：

(1) ngx-echarts Apache图表库

(2) ngx-codemirror 前端语法渲染库

(3) ngx-csv json转csv

[解决]{.underline}

1.  ngx-echarts

    **效果展示**

    ![](https://imgchr.com/i/umy6un){width="4.34375in" height="1.96875in"}

2.  ngx-codemirror

    **效果展示**

    ![](https://imgchr.com/i/umygH0){width="5.768055555555556in"
    height="4.6305555555555555in"}

3.  ngx-csv

    [threshold-plp.component.ts]{.underline}
```typescript
if (data.isExport()) {\
console.log(\"\[table\_top\]opHandler(): EXPORT event triggerred.\");\
new ngxCsv(this.data, \"csv\");\
}
```
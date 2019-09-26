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

![umy6un.png](https://s2.ax1x.com/2019/09/26/umy6un.png)
2.  ngx-codemirror

    **效果展示**

![umygH0.png](https://s2.ax1x.com/2019/09/26/umygH0.png)

3.  ngx-csv

    [threshold-plp.component.ts]{.underline}
```typescript
if (data.isExport()) {\
console.log(\"\[table\_top\]opHandler(): EXPORT event triggerred.\");\
new ngxCsv(this.data, \"csv\");\
}
```
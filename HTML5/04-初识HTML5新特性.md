# 初识HTML5新特性

html的历史和版本，文档类型.

| 时间 | html版本              | 文档类型          | 备注                                   |
| ---- | --------------------- | ----------------- | -------------------------------------- |
| 2000 | html 4.0.1            |                   |                                        |
| 2001 | xhtml 1.0  发展不下去 |                   |                                        |
| 2008 | html 5                | `<!DOCTYPE html>` | 文档声明用于告诉浏览器如何解析该文档。 |



通过 [w3c](http://www.w3school.com.cn/index.html) 查看HTML5新标签和基本特性.



### html5布局新标签和语义

| 标签                  | 语义                  | 备注 |
| --------------------- | --------------------- | ---- |
| `<header></header>`   | 定义页面的页眉和头部. |      |
| `<nav></nav>`         | 定义导航栏            |      |
| `<aside></aside>`     | 定义侧边              |      |
| `<article></article>` | 定义文章              |      |
| `<section></section>` | 定义侧边栏            |      |
| `<footer></footer>`   | 定义底部,叶脚         |      |



### datelist标签

作用:模拟搜索框的提示,结合 input标签使用.

input框使用list属性与 datalist的id属性值进行关联

```
    <input type="text" value="输入明星" list="star" />
    <datalist id="star">
        <option value="张三">张三</option>
        <option value="李四">李四</option>
        <option value="王五">王五</option>
        <option value="前六">前六</option>
    </datalist>
```



### fieldset 标签

作用:进行form表单信息 分组.

```
    <fieldset>
        <legend>用户信息</legend>
        <label >用户名：<input type="text"></label>    <br /> 
        <label >密  码：<input type="password"></label>  <br /> 
    </fieldset>
```



### 表单新增-类型 type

| type                                                    | 案例代码 | 备注                     |
| ------------------------------------------------------- | -------- | ------------------------ |
| email                                                   |          | 需要有@格式的数据        |
| tel                                                     |          | 输入电话                 |
| number                                                  |          | 只能输出数字,有+1,-1操作 |
| url                                                     |          | 需要输入网址             |
| range                                                   |          | 是个滑键,可做音量控制    |
| search                                                  |          | 查询,有删除标志          |
| color                                                   |          | 颜色控件                 |
| 日期<br />(date,moth,time,week,datetime,datetime-local) |          |                          |
|                                                         |          |                          |



### 表单新增-属性

| 属性 | 案例代码 | 作用 |
| ---- | -------- | ---- |
|      |          |      |
|      |          |      |
|      |          |      |
|      |          |      |
|      |          |      |
|      |          |      |



### 表单综合案例


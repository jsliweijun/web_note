# 新增的dom操作api

## 1.获取dom元素

### 1.1 document.querySelector()

入参是选择器：标签，#id，.class 

返回：是页面的第一个元素。



### 1.2 document.querySelectorAll()

入参是选择器：标签，#id，.class 

返回：是页面的一组元素。



## 2.classlist操作元素的class列表

使用如下对应的方法

* add ：添加class值，每次只能添加一个。
* remove ：移除指定的class值。
* toggle ：循环切换class的某个值，有则移除，无则添加。
* contains ：判断class值是否存在。



## 3.给元素添加 data-* 自定义属性

### 3.1 给元素设置自定义属性和值

格式 data-key

注意

- 属性名不应该包含任何大写字母，并且在前缀 "data-" 之后必须有至少一个字符
- 属性值可以是任意字符串
- 不要使用纯数字,特殊字符等作为自定义值
- 如果data之后使用`-`连接多个值,取值时,需要使用`驼峰命名`

### 3.2 获取元素自定义属性的值

- 在js中获取了元素之后,通过  `dom元素对象.dataset["key"]` 即可获取保存的值
- 其中key为`data-xxx`中 xxx的字母
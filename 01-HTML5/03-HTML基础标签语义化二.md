# HTML标签语义化二

主要内容

表格标签

表单标签



## 表格标签

表格的作用：用于数据处理和展示，不要用来做布局。

表格三部分组成：表格外边框 **table**，行 **tr** ，单元格cell **td**。

table的属性

| 属性        | 作用                                      |
| ----------- | ----------------------------------------- |
| border      | 设置表格边框的粗细大小，单元格边框大小。  |
| width       | 设置表格的宽                              |
| height      | 设置表格的高                              |
| align       | 设置表格在页面的位置，left，center，right |
| cellspacing | 设置单元格边框与表格边框的距离            |
| cellpadding | 设置单元格边框与单元格内部内容的距离      |

表格结构，把表格划分成多部分，便于控制。

| 标签                         | 作用     | 备注                                         |
| ---------------------------- | -------- | -------------------------------------------- |
| `<caption>xxx表格</caption>` | 表格标题 |                                              |
| `<thead></thead>`            | 表头     | 表头内容会加粗，单元格标签可以使用`<th><th>` |
| `<tbody></tbody>`            | 表主体   |                                              |

合并单元格

跨行合并：从上往下合并，在最上面的单元格 添加 rowspan=“”  属性值，删除下面的单元格

跨列合并：从左往右合并，在最左边的单元格 添加 colspan=“”  属性值，删除右边的单元格



## 表单

表单用于填写数据，并将数据传输到后台的标签。

收集用户信息。



表单的组成部分：表单域，提示信息，表单控件。



### 表单控件

#### input 标签控件

是单标签，通过 type属性进行设置控件类型。具体值有如下：

* 文本框控件  type="text"

```
<input type="text" maxlength=“6”  vaule="显示内容" />   用于进行账号内容的填写
```

* 密码控件  type=“password”

```
<input type="password">  用于密码输入
```

* 单选框，通过加checked="checked" 设置默认值.

```
<input type="radio" name="sex">  进行单选值的选择，多个单选框需要通过name属性设置相同
```

* 复选框，通过加checked="checked" 设置默认值.

```
<input type="checkbox" name="hobbit">  先进多项选择时使用，name属性进行分组。
```

* 按钮组 ，button，submit，reset，img，file

| type                                       | 作用             | 备注                                |
| ------------------------------------------ | ---------------- | ----------------------------------- |
| `<input type="button" value="普通按钮" />` | 用于显示一个按钮 | 需要使用value属性进行显示，按钮的值 |
| `<input type="submit" />`                  | 提交按钮         |                                     |
| `<input type="submit" />`                  | 重置按钮         |                                     |
| `<input type="img" src="imgBnt.jpg" />`    | 图片按钮         | 需要使用 src 属性引入图片           |
| `<input type="file" />`                    | 文件按钮         | 显示一个可上传的控件                |



#### label标签

用于点击 `提示信息` 方便定位到具体控件上，提高用户体验。

方式一：直接使用label标签包裹 提示信息 + 表单控件

```
<label>用户名：<input type="text" /></label>  当点击用户名时 光标会自动到 文本框中
```

方式二：当label标签中有多个表单控件时，使用 for id 的方式指定 点击 提示信息后 定位到 具体的 表单控件。

```
<label for="two">用户名：<input type="text" /> <input type="text" id="two" /></label>  当点击用户名时 光标会自动到 第2个文本框中
```



#### textarea标签 (文本域)

用于可输入多行数据的控件，例如用在 留言板的实现。 它是双标签

```
<textarea>请输出留言内容</textarea>  它的长和宽使用css来进行控制。
```



#### select标签（下拉菜单）

用于实现下拉选择，如 省 市  区 的下拉选择。

```
<select>
	<option></option>
	<option></option>
</select>
```

1.下拉菜单需要包含有 option 选项。

2.给option选项设置 selected=“selected” 属性后为默认选项值。



#### form标签  表单域

进行包裹提示信息+表单控件的，配合 submit，reset 按钮功能使用。

```
<form action="url" method="post" name="userMassage" >


</form>
```

action：填写具体的后台接口url。

method：请求方式，get，post。

name：给表单起个名字。


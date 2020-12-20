# HTML5的认识和兼容性处理方式

## 认识html5。

html5：是html的第5版本。如今浏览器对html5的支持度都越来越高，开发需要不断学习和使用它。

![什么是html5](D:\study\web_note\file\什么是html5.png)



## h5语义标签的使用

[查看现有标签](http://www.w3school.com.cn/tags/html_ref_byfunc.asp)

在html5中，进行了新增语义特性功能，就是增加了新的有语义的标签：

​	语义标签如：img->图片标签，见标签名就知道其作用。

平常使用div进行布局，如今可以使用以下

​	header->头部标签

​	main->主体部分标签

​	footer->脚部标签

 如下图常用的布局标签

![](D:\study\web_note\file\h5语义化特性-新增语义标签.png)

使用了语义化标签后的实现案例

![](D:\study\web_note\file\语义前.png)

![](D:\study\web_note\file\语义后.png)

看标签就可知道具体内容。



## h5语义标签的兼容性处理，2种方式

主流浏览器

​	支持h5，很好展示。

ie浏览器

​	edge 完全支持 h5标签。

​	ie9-ie11 支持部分h5标签，布局标签当做行级标签展示。**行级标签设置高和宽是无效的**  加 display：block。

​	ie8完全不支持h5新标签。

方式一：手动创建标签,创建的是行级元素，需要加样式 display：block

```javascript
<!-- 解决ie8以下版本兼容h5新标签 -->
<!-- 方式1 -->
        <script>
            document.createElement("header");
            document.createElement("nav");
            document.createElement("main");
            document.createElement("aside");
            document.createElement("article");
            document.createElement("footer");
        </script>
```

方式二：引入js库，html5shiv.min.js

```javascript
<!-- 方式2，引入第三方js库 -->
<script src="../lib/html5shiv.min.js"></script>
```


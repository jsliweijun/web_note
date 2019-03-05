# jQuery初识

## 出现jQuery的原因

使用原生js时会有如下缺点。

![](..\file\06-原生js的缺陷.png)

面对这些缺点，就出现了 [jQuery库](https://jquery.com/)。

如何使用jQuery库

* 引入jQuery库
* 学习使用jQuery提供的 api方法，进行操作dom，实现响应的功能。



## 学习jQuery

### jQuery的入口函数

1. 有两种 **入口函数 ** 方式

```
<script src="./jquery-1.12.3.js"></script>
<script>
    //方式一
    $(document).ready(function(){
        console.log("jQuery 入口函数1");
    });

    //方式二
    $(function(){
        console.log("jQuery 入口函数2");
    });
</script>
```

2. 入口函数与原生js的 window.onload=function(){} 的区别

* window.onload 只能加载一次，因为会出现覆盖的情况。



### $和jQuery对象的认识，它们都是一个 函数

1. $是什么?



2. jQuery文件的结构





### jQuery对象与dom对象














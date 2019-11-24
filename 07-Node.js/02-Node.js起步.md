# 起步

## 下载

lts 长期支持版，稳定版

current 最新版

## 安装，查看版本

```shell
node --version 
```

## node 运行js文件

```shell
node xxx.js
```

## helloworld演示简单的知识点

1. 解析js文件，对比node与浏览器中的js。node 中没有DOM，BOM，没有以下对象  window，document 。

2. node中的读写文件 API ，使用 require 方法加载 **fs** 核心模块。

   ```
   var fs = require("fs");
   ```

3. http 服务器，Node构建一个 Web 服务器，Node 提供核心模块 **http** 提供服务server ，4步实现基本功能。

   1. 接收请求 request
   2. 发送响应 response。write("xx") 返回信息给页面，要使用 end 来结束响应。




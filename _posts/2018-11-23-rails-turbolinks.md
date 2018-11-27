---
title: Turbolinks5 概述及实现原理
layout: post
tags: rails
---

[https://yafeilee.me/blogs/88(https://yafeilee.me/blogs/88](https://yafeilee.me/blogs/88(https://yafeilee.me/blogs/88)

解决跳转页面不加载的问题
将需要初始化的代码添加到window.init中
然后在body中调用该变量

```
<script>
      $(document).ready(window.init)
    </script>
```
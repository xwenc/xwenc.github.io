---
title: Assets pipeline 使用 package 中第三方插件
layout: post
tag: rails
---

1. 通过 yarn add 之后，使用这样的方式引用 js ，
```
//= require select2/dist/js/select2
```
 node_modules 的
2. 使用这样的方式引用 css ，
```
@import "select2/dist/css/select2";
```
路径同样是相对于 node_modules 的.

3.require_tree 的意思是，把当前目录的 js 文件都引用进来，所以，要在相同目录下，每一个 controller 都建一个 js 文件，放对应的页面的 js 逻辑
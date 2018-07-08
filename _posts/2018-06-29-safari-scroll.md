---
title: 'iOS Safari浏览器上overflow: scroll元素无法滑动bug解决方法整理'
layout: post
tags: frontend
---

1. 必须为所有在移动端的overflow: scroll元素增加属性 -webkit-overflow-scrolling: touch。
当父元素可不脱离文档流时不要脱离文档流。
2. 在子元素iframe加载完成后可异步将父元素的overflow: scroll属性重写（此方法可能不成功）。
3. 如以上没有解决，则给予子元素一个min-height，大小不限（略大于效果最好），帮助safari建立ScrollView（亲测最有效）。
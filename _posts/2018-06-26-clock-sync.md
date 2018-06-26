---
title: 彻底弄懂客户端时间和服务器同步
layout: post
tags: algorithm
---

这里的算法有点问题，需要做精确一点

客户端时间是错的，发起请求，为客户端认为的第A=100秒
服务端接收到数据的时候，时间是第X=150秒
服务器非常慢，回复给客户端的时候，时间是第Y=160秒
客户端接收到数据，这时候是客户端认为的第B=120秒

客户端计算网络延迟为 B - A - (服务器响应时间) = B - A - (Y - X) = 10秒

客户端认为发起的延迟和返回的延迟相同，所以，从服务端返回到客户端的延迟就是 10 / 2 = 5秒
所以，客户端认为，客户端接收到返回的真实时间是 160 + 5 = 165秒，所以，客户端时间差 = 165 - 120 = 45秒

所以真实的A是 = 145， 真实的B = 165
按照这个算法，把服务器的响应时间也计算进去，精确到毫秒吧至少

[https://stackoverflow.com/questions/1638337/the-best-way-to-synchronize-client-side-javascript-clock-with-server-date](https://stackoverflow.com/questions/1638337/the-best-way-to-synchronize-client-side-javascript-clock-with-server-date)

![时间同步](/assets/images/2018-06-26-01.png)
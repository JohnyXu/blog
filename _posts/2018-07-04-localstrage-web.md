---
layout: post
title: 网页 LocalStorage 存储知多少
categories: Web
description: 网页缓存容量测试
keywords: Web,Storage
---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**网页缓存容量测试**  *localstorage*

- [LocalStorage 容量测试](#localstorage-%E5%AE%B9%E9%87%8F%E6%B5%8B%E8%AF%95)
  - [测试代码](#%E6%B5%8B%E8%AF%95%E4%BB%A3%E7%A0%81)
- [各个浏览器支持容量大小](#%E5%90%84%E4%B8%AA%E6%B5%8F%E8%A7%88%E5%99%A8%E6%94%AF%E6%8C%81%E5%AE%B9%E9%87%8F%E5%A4%A7%E5%B0%8F)
  - [PC](#pc)
  - [Mobile](#mobile)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


# LocalStorage 容量测试

## 测试代码
```js
(function () {
    if (!window.localStorage) {
        console.log('当前浏览器不支持localStorage!')
    }
    var test = '0123456789';
    var add = function (num) {
        num += num;
        if (num.length == 10240) {
            test = num;
            return;
        }
        add(num);
    }
    add(test);
    var sum = test;
    var show = setInterval(function () {
        sum += test;
        try {
            window.localStorage.removeItem('test');
            window.localStorage.setItem('test', sum);
            console.log(sum.length / 1024 + 'KB');
        } catch (e) {
            alert(sum.length / 1024 + 'KB超出最大限制');
            clearInterval(show);
        }
    }, 0.1)
})()
```

# 各个浏览器支持容量大小
## PC
```
Chrome:5120Kb
QQ浏览器:5120Kb
360浏览器:5120Kb
搜狗浏览器:5120Kb
```

## Mobile
```
手机QQ内置浏览器：5120Kb
手机微信内置浏览器：5120Kb
搜狗浏览器：510Kb(会崩溃)-> 720Kb
Chrome: 5120Kb
```
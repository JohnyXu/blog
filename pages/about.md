---
layout: page
title: About
description: 一只翱翔于蓝天的小菜鸟
keywords: Qiang Xu,徐强
comments: false
menu: 关于
permalink: /about/
---

一只翱翔于蓝天的小菜鸟，在不停的吸收经验。
坚信熟能生巧，努力改变人生。

## 联系

{% for website in site.data.social %}
* {{ website.sitename }}：[@{{ website.name }}]({{ website.url }})
{% endfor %}

## Skill Keywords

{% for category in site.data.skills %}
### {{ category.name }}
<div class="btn-inline">
{% for keyword in category.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}

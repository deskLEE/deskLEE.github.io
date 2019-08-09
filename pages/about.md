---
layout: page
title: About
description: 学习可以提高自己
keywords: deskLEE, 胡枝子
comments: true
menu: 关于
permalink: /about/
---

小白

微电子专业 电子信息工程专业。

提升自我的能力。

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

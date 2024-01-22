---
layout: page
title: About
description: 打码改变世界
keywords: Zhuang Ma, 马壮
comments: true
menu: 关于
permalink: /about/
---

我是朱佳纯（Jaycee Zhu）,1998年出生于广东汕头一个沿海渔村。爱好摄影，读书，写作和运动。2020开始记录生活至今。

目前在深圳从事海外营销的工作，希望自己成为海外营销的专家。

做这个博客的原因是我喜欢写作和思考，我希望把我的思考和经验分享给所有人，记录我平凡的生活，在我八十岁的时候可以看到我年轻美好的记忆。

## 联系

<ul>
{% for website in site.data.social %}
<li>{{website.sitename }}：<a href="{{ website.url }}" target="_blank">@{{ website.name }}</a></li>
{% endfor %}
{% if site.url contains 'jaycee-zhu.github.io' %}
<li>
微信公众号：<br />
<img style="height:192px;width:192px;border:1px solid lightgrey;" src="{{ site.url }}/assets/images/qrcode.jpg" alt="朱佳纯" />
</li>
{% endif %}
</ul>


## Skill Keywords

{% for skill in site.data.skills %}
### {{ skill.name }}
<div class="btn-inline">
{% for keyword in skill.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}

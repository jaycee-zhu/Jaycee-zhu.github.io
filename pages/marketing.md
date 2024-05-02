---
layout: marketing
title: 海外市场营销
description: 欢迎访问我的专业分享页面！在这里我将与大家探讨海外营销的多个重要领域，包括建站、搜索引擎优化（SEO）、搜索引擎营销（SEM）、社交媒体策略、红人推广、展会营销、亚马逊联盟、社群管理、营销策划方案、海外B2B推广以及产品管理等内容。
keywords: 海外市场营销
comments: true
mermaid: true
menu: 片段
permalink: /marketing/
---

> 欢迎访问我的专业分享页面！在这里我将与大家探讨海外营销的多个重要领域，包括建站、搜索引擎优化（SEO）、搜索引擎营销（SEM）、社交媒体策略、红人推广、展会营销、亚马逊联盟、社群管理、营销策划方案、海外B2B推广以及产品管理等内容。

{% assign tagliststr = '' %}
{% for item in site.marketing %}
{% if item.title != "marketing Template" %}
  {% for tag in item.tags %}
    {% if tagliststr contains tag %}
    {% else %}
      {% if tagliststr != '' %}{% assign tagliststr = tagliststr | append: ',' %}{% endif %}
      {% assign tagliststr = tagliststr | append: tag %}
    {% endif %}
  {% endfor %}
{% endif %}
{% endfor %}

{% assign taglist = tagliststr | split: ',' | sort_natural %}

<a href="{{ site.url }}/marketing/" style="color:#888;display:inline-block;margin:0 8px;">全部</a>{% for tag in taglist %}<a href="{{ site.url }}/marketing/?tag={{ tag }}" style="color:#888;display:inline-block;margin:0 8px;">{{ tag }}</a>{% endfor %}

<ul class="listing">
{% for item in site.marketing %}
{% if item.title != "marketing Template" %}
<li class="listing-item" tags="{% for tag in item.tags %}{{ tag }} {% endfor %}">
  <a href="{{ site.url }}{{ item.url }}">{{ item.title }}</a>
  {% for tag in item.tags %}
  <a style="font-size:12px;color:gray;font-style:italic;display:inline-block;margin:0 0 0 4px;padding:0 4px;background-color:lightgray;" href="{{ site.url }}/marketing/?tag={{ tag }}" title="{{ tag }}">{{ tag }}</a>
  {% endfor %}
</li>
{% endif %}
{% endfor %}
</ul>

<script>
jQuery(function() {
    function getUrlParam(name) {
        var reg = new RegExp("(^|&)" + name + "=([^&]*)(&|$)");
        var r = window.location.search.substr(1).match(reg);
        if (r != null) return r[2]; return null;
    }

    var tag = getUrlParam('tag');
    if (tag == undefined || tag === '') {
        return;
    }

    $(".listing-item").each(function() {
        if ($(this).attr('tags').indexOf(tag) < 0) {
            $(this).css('display', 'none');
        }
    });

});
</script>

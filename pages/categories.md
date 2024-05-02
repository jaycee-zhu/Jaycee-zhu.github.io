---
<<<<<<< HEAD
<<<<<<< HEAD:pages/diary.md
layout: page
title: Diary
=======
layout: categories
title: Categories
>>>>>>> parent of 3c1a69485 (更改):pages/categories.md
description: 哈哈，你找到了我的文章基因库
keywords: 分类
comments: false
<<<<<<< HEAD:pages/diary.md
menu: 个人成长
permalink: /diary/
=======
menu: 分类
permalink: /categories/
>>>>>>> parent of 3c1a69485 (更改):pages/categories.md
=======
layout: categories
title: Categories
description: 哈哈，你找到了我的文章基因库
keywords: 分类
comments: false
menu: 分类
permalink: /categories/
>>>>>>> parent of 3c1a69485 (更改)
---

<section class="container posts-content">
{% assign sorted_categories = site.categories | sort %}
{% for category in sorted_categories %}
<h3 id="{{ category[0] }}">{{ category | first }}</h3>
<ol class="posts-list">
{% for post in category.last %}
<li class="posts-list-item">
<span class="posts-list-meta">{{ post.date | date:"%Y-%m-%d" }}</span>
<a class="posts-list-name" href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
</li>
{% endfor %}
</ol>
{% endfor %}
</section>
<!-- /section.content -->

---
title: "新闻动态"
layout: gridlay
sitemap: false
permalink: /allnews.html
---

## 新闻动态

<div class="section-card" markdown="0">
<div class="news-timeline">
{% for article in site.data.news %}
<div class="news-item">
<span class="news-date">{{ article.date }}</span>
<span class="news-headline">{{ article.headline }}</span>
</div>
{% endfor %}
</div>
</div>

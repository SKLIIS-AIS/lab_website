---
title: "News"
layout: gridlay
sitemap: false
permalink: /en/allnews.html
lang: en
translation_url: /allnews.html
---

## News and Updates

<div class="section-card" markdown="0">
<div class="news-timeline">

{% for article in site.data.news %}
<div class="news-item">
<span class="news-date">{{ article.date_en | default: article.date }}</span>
<span class="news-headline">{{ article.headline_en | default: article.headline }}</span>
</div>
{% endfor %}

</div>
</div>

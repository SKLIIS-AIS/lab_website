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

<span class="news-date">
{% if article.date_en %}
{{ article.date_en }}
{% else %}
{{ article.date }}
{% endif %}
</span>

<span class="news-headline">
{% if article.headline_en %}
{{ article.headline_en }}
{% else %}
{{ article.headline }}
{% endif %}
</span>

</div>
{% endfor %}

</div>
</div>

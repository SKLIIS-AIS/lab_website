---
title: Publications
layout: publications
sitemap: false
permalink: /en/publications/
lang: en
translation_url: /publications/
---

## 论文成果

<input type="text" class="pub-search" id="pubSearch" placeholder="按标题、作者或年份筛选论文...">

<div class="section-card" id="pubList">

{% comment %}
<h3>预印本</h3>

{% bibliography --query @unpublished %}
{% endcomment %}

<h3>期刊论文</h3>

{% bibliography --query @article %}

<h3>会议论文</h3>

{% bibliography --query @inproceedings %}

</div>


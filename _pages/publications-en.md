---
title: Publications
layout: publications
sitemap: false
permalink: /en/publications/
lang: en
translation_url: /publications/
---

## Paper Result

<input type="text" class="pub-search" id="pubSearch" placeholder="按标题、作者或年份筛选论文...">

<div class="section-card" id="pubList">

{% comment %}
## Arxiv

{% bibliography --query @unpublished %}
{% endcomment %}

## Journal Articles

{% bibliography --query @article %}

## Conference Papers

{% bibliography --query @inproceedings %}

</div>


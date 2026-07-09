---
title: "学术报告"
layout: gridlay
sitemap: false
permalink: /talks/
---

## 学术报告

<div class="section-card" id="pubList">
<h3>邀请报告</h3>

{% bibliography --query @incollection[keywords ^= invited] %}

<h3>其他报告</h3>

{% bibliography --query @incollection[keywords != invited] %}
</div>

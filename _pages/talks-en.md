---
title: "Talks"
layout: gridlay
sitemap: false
permalink: /en/talks/
lang: en
translation_url: /talks/
---

## Academic Talks

<div class="section-card" id="pubList">
<h3>Invited Talks</h3>

{% bibliography --query @incollection[keywords ^= invited] %}

<h3>Other Talks</h3>

{% bibliography --query @incollection[keywords != invited] %}
</div>

---
title: "关于老师"
layout: gridlay
sitemap: false
permalink: /about/
---

## 关于老师

<div class="section-card">
<div class="pi-card">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ site.data.pi[0].photo }}" class="pi-photo" alt="{{ site.data.pi[0].name }}" loading="lazy">

<div>
<h3 class="pi-name">{{ site.data.pi[0].name }}</h3>

<p style="font-style: italic; color: var(--text-secondary);">
{{ site.data.pi[0].title }}，{{ site.data.pi[0].institution }}
</p>

<p style="color: var(--text-secondary);">
{{ site.data.pi[0].lab }}
</p>

<p>
<strong>学科：</strong>{{ site.data.pi[0].discipline }}<br>
<strong>研究方向：</strong>{{ site.data.pi[0].research }}
</p>

<div class="pi-links">
<a href="mailto:{{ site.data.pi[0].email }}" class="icon-link" title="发送邮件">
<i class="fa-solid fa-envelope"></i>
</a>

<a href="{{ site.data.pi[0].homepage }}" class="icon-link" title="教师主页" target="_blank">
<i class="fa-solid fa-house"></i>
</a>
</div>

<p style="margin-top: var(--space-3);">
邮箱：<a href="mailto:{{ site.data.pi[0].email }}">{{ site.data.pi[0].email }}</a>
</p>

{% if site.data.pi[0].education %}
<ul style="margin-top: var(--space-4);">
{% for education in site.data.pi[0].education %}
<li>{{ education | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
{% endif %}
</div>
</div>
</div>

{% if site.data.grants %}
<div class="section-card">
<h3>科研项目</h3>
<ul>
{% for grant in site.data.grants %}
<li>{{ grant.name }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.awards %}
<div class="section-card">
<h3>获奖情况</h3>
<ul>
{% for award in site.data.awards %}
<li>{{ award.name | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.people %}
<div class="section-card">
<h3>学生培养</h3>
<ul>
{% for student in site.data.people %}
<li>{{ student.name }}, {{ student.location }} ({{ student.degree }}, {{ student.year }})</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.funders %}
<div class="section-card">
<h4>基金情况</h4>
<div class="sponsor-logos" style="display: flex; flex-wrap: wrap; align-items: center; justify-content: center; gap: var(--space-6);">
{% for funder in site.data.funders %}
<a href="{{ funder.url }}" target="_blank"><img src="{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}" alt="Funder logo" style="max-height: 80px; max-width: 200px; border-radius: 0;" loading="lazy"></a>
{% endfor %}
</div>
</div>
{% endif %}

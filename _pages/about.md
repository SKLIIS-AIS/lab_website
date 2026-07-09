---
title: "关于老师"
layout: gridlay
sitemap: false
permalink: /about/
---

## 关于老师

<div class="section-card" markdown="0">
<div style="display: grid; grid-template-columns: 260px 1fr; gap: 2.5rem; align-items: start;">

<div style="text-align: center;">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ site.data.pi[0].photo }}" alt="{{ site.data.pi[0].name }}" loading="lazy" style="width: 220px; height: 280px; object-fit: cover; object-position: center; border-radius: 16px; border: 1px solid var(--border-color); box-shadow: var(--shadow-sm);">

<div style="margin-top: 1rem;">
<a href="{{ site.data.pi[0].homepage }}" target="_blank" style="display: inline-block; padding: 0.45rem 0.9rem; border: 1px solid var(--accent-color); border-radius: 999px; color: var(--accent-color); text-decoration: none; font-size: 0.95rem;">
教师主页
</a>
</div>
</div>

<div>
<h2 style="margin-top: 0; margin-bottom: 0.5rem;">{{ site.data.pi[0].name }}</h2>

<p style="font-size: 1.05rem; color: var(--text-secondary); margin-bottom: 0.5rem;">
{{ site.data.pi[0].title }}
</p>

<p style="color: var(--text-secondary); margin-bottom: 0.5rem;">
{{ site.data.pi[0].institution }}
</p>

<p style="color: var(--text-secondary); margin-bottom: 1.25rem;">
{{ site.data.pi[0].lab }}
</p>

<div style="display: grid; grid-template-columns: 5rem 1fr; row-gap: 0.6rem; column-gap: 0.75rem; margin-bottom: 1.25rem;">
<strong>学科</strong>
<span>{{ site.data.pi[0].discipline }}</span>

<strong>研究方向</strong>
<span>{{ site.data.pi[0].research }}</span>

<strong>邮箱</strong>
<span><a href="mailto:{{ site.data.pi[0].email }}">{{ site.data.pi[0].email }}</a></span>
</div>

{% if site.data.pi[0].education %}
<div style="margin-top: 1.25rem; padding-top: 1.25rem; border-top: 1px solid var(--border-color);">
<h3 style="margin-top: 0; margin-bottom: 0.75rem; font-size: 1.15rem;">教育与工作经历</h3>
<ul style="margin-bottom: 0;">
{% for education in site.data.pi[0].education %}
<li>{{ education | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
</div>
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

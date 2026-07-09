---
title: "关于老师"
layout: gridlay
sitemap: false
permalink: /about/
---

## 关于老师

<div class="section-card teacher-profile" markdown="1">

<div class="teacher-photo-wrap">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ site.data.pi[0].photo }}" alt="{{ site.data.pi[0].name }}" class="teacher-photo" loading="lazy">
  <p class="teacher-homepage">
    <a href="{{ site.data.pi[0].homepage }}" target="_blank">教师主页</a>
  </p>
</div>

<div class="teacher-info">

### {{ site.data.pi[0].name }}

{{ site.data.pi[0].title }}

{{ site.data.pi[0].institution }}

{{ site.data.pi[0].lab }}

| 项目 | 信息 |
|---|---|
| 学科 | {{ site.data.pi[0].discipline }} |
| 研究方向 | {{ site.data.pi[0].research }} |
| 邮箱 | [{{ site.data.pi[0].email }}](mailto:{{ site.data.pi[0].email }}) |

{% if site.data.pi[0].education %}

#### 教育与工作经历

{% for education in site.data.pi[0].education %}
- {{ education | replace: "-","&#8211;" }}
{% endfor %}

{% endif %}

</div>

</div>

<style>
.teacher-profile {
  display: grid;
  grid-template-columns: 260px 1fr;
  gap: 2.5rem;
  align-items: start;
  padding: 2rem 2.5rem;
}

.teacher-photo-wrap {
  text-align: center;
}

.teacher-photo {
  width: 220px;
  height: 280px;
  object-fit: cover;
  object-position: center;
  border-radius: 16px;
  border: 1px solid var(--border-color);
  box-shadow: var(--shadow-sm);
}

.teacher-homepage {
  margin-top: 1rem;
}

.teacher-homepage a {
  display: inline-block;
  padding: 0.45rem 0.9rem;
  border: 1px solid var(--accent-color);
  border-radius: 999px;
  color: var(--accent-color);
  text-decoration: none;
  font-size: 0.95rem;
}

.teacher-info h3 {
  margin-top: 0;
}

.teacher-info table {
  margin-top: 1.25rem;
  margin-bottom: 1.5rem;
}

@media (max-width: 768px) {
  .teacher-profile {
    grid-template-columns: 1fr;
    padding: 1.5rem;
  }

  .teacher-photo {
    width: 200px;
    height: 260px;
  }
}
</style>

{% if site.data.grants %}
<div class="section-card" markdown="1">

### 科研项目

{% for grant in site.data.grants %}
- {{ grant.name }}
{% endfor %}

</div>
{% endif %}

{% if site.data.awards %}
<div class="section-card" markdown="1">

### 获奖情况

{% for award in site.data.awards %}
- {{ award.name | replace: "-","&#8211;" }}
{% endfor %}

</div>
{% endif %}

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

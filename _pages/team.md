---
title: "团队成员"
layout: gridlay
sitemap: false
permalink: /team/
---

## 团队成员

<div class="section-card" style="border-left: 4px solid var(--accent-color); padding: 1.25rem 1.5rem; margin: 1.5rem 0 2rem 0;">
  <h3 style="margin-top: 0; margin-bottom: 0.75rem;">加入我们</h3>
  <p style="margin-bottom: 0;">
    课题组长期欢迎对工业互联网安全、人工智能安全、网络空间安全和数据安全等方向感兴趣的本科生、硕士生、博士生及科研合作伙伴加入或交流。
  </p>
</div>

## 课题组负责人

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
</div>
</div>
</div>

{% if site.data.team_members.size > 0 %}
## 在组成员

<div class="team-grid">
{% for member in site.data.team_members %}
<div class="team-card">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" class="team-photo" alt="{{ member.name }}" loading="lazy">
<h4 class="team-name">{{ member.name }}</h4>
<p class="team-info">{{ member.info }}</p>
<div class="team-links">
{% if member.email %}<a href="mailto:{{ member.email }}" class="icon-link" title="邮箱"><i class="fa-solid fa-envelope"></i></a>{% endif %}
{% if member.website %}<a href="{{ member.website }}" class="icon-link" title="个人主页"><i class="fa-solid fa-house"></i></a>{% endif %}
{% if member.scholar %}<a href="{{ member.scholar }}" class="icon-link" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
{% if member.github %}<a href="{{ member.github }}" class="icon-link" title="GitHub"><i class="fa-brands fa-github"></i></a>{% endif %}
</div>
</div>
{% endfor %}
</div>
{% endif %}

{% if site.data.alumni.size > 0 %}
## 毕业生与离组成员

<div class="section-card">
<table class="alumni-table">
<thead>
<tr><th>姓名</th><th>在组时间</th><th>当前去向</th></tr>
</thead>
<tbody>
{% for member in site.data.alumni %}
<tr>
<td>{{ member.name }}</td>
<td>{{ member.duration }}</td>
<td>{{ member.info }}</td>
</tr>
{% endfor %}
</tbody>
</table>
</div>
{% endif %}

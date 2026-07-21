---
title: "Team Members"
layout: gridlay
sitemap: false
permalink: /en/team/
lang: en
translation_url: /team/
---

## Team Members

<div class="section-card" style="border-left: 4px solid var(--accent-color); padding: 1.25rem 1.5rem; margin: 1.5rem 0 2rem 0;">
<h3 style="margin-top: 0; margin-bottom: 0.75rem;">Join Us</h3>
<p style="margin-bottom: 0;">
The AIS Research Group welcomes undergraduate students, master's students, doctoral students, and research collaborators interested in Industrial Internet security, artificial intelligence security, cyberspace security, data security, and related research areas.
</p>
</div>

## Principal Investigator

<div class="section-card">
<div class="pi-card">

<img src="{{ site.url }}{{ site.baseurl }}/images/{{ site.data.pi[0].photo }}"
     class="pi-photo"
     alt="{{ site.data.pi[0].name_en | default: site.data.pi[0].name }}"
     loading="lazy">

<div>
<h3 class="pi-name">
{{ site.data.pi[0].name_en | default: site.data.pi[0].name }}
</h3>

<p style="font-style: italic; color: var(--text-secondary);">
{{ site.data.pi[0].title_en | default: site.data.pi[0].title }},
{{ site.data.pi[0].institution_en | default: site.data.pi[0].institution }}
</p>

<p style="color: var(--text-secondary);">
{{ site.data.pi[0].lab_en | default: site.data.pi[0].lab }}
</p>

<p>
<strong>Discipline:</strong>
{{ site.data.pi[0].discipline_en | default: site.data.pi[0].discipline }}
<br>

<strong>Research Interests:</strong>
{{ site.data.pi[0].research_en | default: site.data.pi[0].research }}
</p>

{% if site.data.pi[0].homepage %}
<div class="pi-links">
<a href="{{ site.data.pi[0].homepage }}"
   class="icon-link"
   title="Faculty Homepage"
   aria-label="Faculty Homepage"
   target="_blank"
   rel="noopener noreferrer">
<i class="fa-solid fa-house"></i>
</a>
</div>
{% endif %}

{% if site.data.pi[0].email %}
<p style="margin-top: var(--space-3);">
<strong>Email:</strong>
<a href="mailto:{{ site.data.pi[0].email | strip }}">
{{ site.data.pi[0].email }}
</a>
</p>
{% endif %}

</div>
</div>
</div>

{% if site.data.team_members and site.data.team_members.size > 0 %}

## Current Members

<div class="team-grid" markdown="0">

{% for member in site.data.team_members %}

<div class="team-card">

<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}"
     class="team-photo"
     alt="{{ member.name_en | default: member.name }}"
     loading="lazy">

<h4 class="team-name">
{{ member.name_en | default: member.name }}
</h4>

<p class="team-info">
{{ member.info_en | default: member.info }}
</p>

{% if member.research_en or member.research %}
<p class="team-info">
<strong>Research Interests:</strong>
{{ member.research_en | default: member.research }}
</p>
{% endif %}

{% if member.email and member.email != "" %}
<div class="team-email">
<a href="mailto:{{ member.email | strip }}"
   title="Send an email to {{ member.name_en | default: member.name }}">

<i class="fa-solid fa-envelope"></i>

<span>{{ member.email }}</span>
</a>
</div>
{% endif %}

{% if member.website or member.scholar or member.github %}
<div class="team-links">

{% if member.website %}
<a href="{{ member.website }}"
   class="icon-link"
   title="Personal Website"
   aria-label="Personal Website"
   target="_blank"
   rel="noopener noreferrer">
<i class="fa-solid fa-house"></i>
</a>
{% endif %}

{% if member.scholar %}
<a href="{{ member.scholar }}"
   class="icon-link"
   title="Google Scholar"
   aria-label="Google Scholar"
   target="_blank"
   rel="noopener noreferrer">
<i class="ai ai-google-scholar"></i>
</a>
{% endif %}

{% if member.github %}
<a href="{{ member.github }}"
   class="icon-link"
   title="GitHub"
   aria-label="GitHub"
   target="_blank"
   rel="noopener noreferrer">
<i class="fa-brands fa-github"></i>
</a>
{% endif %}

</div>
{% endif %}

</div>

{% endfor %}

</div>

{% endif %}

## Alumni and Former Members

{% if site.data.alumni and site.data.alumni.size > 0 %}

<div class="section-card">

<table class="alumni-table">

<thead>
<tr>
<th>Name</th>
<th>Period in the Group</th>
<th>Current Position</th>
</tr>
</thead>

<tbody>

{% for member in site.data.alumni %}

<tr>
<td>{{ member.name_en | default: member.name }}</td>
<td>{{ member.duration_en | default: member.duration }}</td>
<td>{{ member.info_en | default: member.info }}</td>
</tr>

{% endfor %}

</tbody>

</table>

</div>

{% else %}

<div class="section-card">
<p style="margin: 0; color: var(--text-secondary); text-align: center;">
No alumni or former members are currently listed.
</p>
</div>

{% endif %}

<style>
.team-email {
  width: 100%;
  margin-top: 0.65rem;
  padding-top: 0.65rem;
  border-top: 1px solid var(--border-color);
  text-align: center;
}

.team-email a {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.35rem;
  padding: 0 0.35rem;
  color: var(--text-secondary);
  text-decoration: none;
  font-size: 0.7rem;
  line-height: 1.35;
  overflow-wrap: anywhere;
  word-break: break-word;
}

.team-email a:hover {
  color: var(--accent-color);
}

.team-email i {
  flex: 0 0 auto;
  font-size: 0.8rem;
}

.team-email span {
  min-width: 0;
}

@media (max-width: 768px) {
  .team-email a {
    font-size: 0.76rem;
  }
}
</style>

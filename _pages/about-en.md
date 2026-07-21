---
title: "About"
layout: gridlay
sitemap: false
permalink: /en/about/
lang: en
translation_url: /about/
---

## About the Principal Investigator

<div class="section-card teacher-profile" markdown="1">

<div class="teacher-photo-wrap">
  <img
    src="{{ site.url }}{{ site.baseurl }}/images/{{ site.data.pi[0].photo }}"
    alt="{{ site.data.pi[0].name_en | default: site.data.pi[0].name }}"
    class="teacher-photo"
    loading="lazy">

  {% if site.data.pi[0].homepage %}
  <p class="teacher-homepage">
    <a
      href="{{ site.data.pi[0].homepage }}"
      target="_blank"
      rel="noopener noreferrer">
      Faculty Homepage
    </a>
  </p>
  {% endif %}
</div>

<div class="teacher-info">

### {{ site.data.pi[0].name_en | default: site.data.pi[0].name }}

{{ site.data.pi[0].title_en | default: site.data.pi[0].title }}

{{ site.data.pi[0].institution_en | default: site.data.pi[0].institution }}

{{ site.data.pi[0].lab_en | default: site.data.pi[0].lab }}

<div class="teacher-basic-info" markdown="0">

<p>
  <strong>Discipline:</strong>
  {{ site.data.pi[0].discipline_en | default: site.data.pi[0].discipline }}
</p>

<p>
  <strong>Research Interests:</strong>
  {{ site.data.pi[0].research_en | default: site.data.pi[0].research }}
</p>

{% if site.data.pi[0].email %}
<p>
  <strong>Email:</strong>
  <a href="mailto:{{ site.data.pi[0].email }}">
    {{ site.data.pi[0].email }}
  </a>
</p>
{% endif %}

</div>

{% assign education_list = site.data.pi[0].education_en | default: site.data.pi[0].education %}

{% if education_list %}

#### Education and Professional Experience

{% for education in education_list %}
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

.teacher-homepage a:hover {
  background-color: var(--accent-color);
  color: #ffffff;
  text-decoration: none;
}

.teacher-info h3 {
  margin-top: 0;
}

.teacher-basic-info {
  margin-top: 1.25rem;
  margin-bottom: 1.5rem;
  line-height: 1.9;
}

.teacher-basic-info p {
  margin: 0.15rem 0;
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
<div class="section-card">
<h3>Research Projects</h3>
<ul>
{% for grant in site.data.grants %}
<li>{{ grant.name_en | default: grant.name }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.awards %}
<div class="section-card">
<h3>Research Achievements</h3>
<ul>
{% for award in site.data.awards %}
<li>{{ award.name_en | default: award.name | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.people %}
<div class="section-card">
<h3>Student Recruitment</h3>
<ul>
{% for student in site.data.people %}
<li>{{ student.name_en | default: student.name }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% comment %}
{% if site.data.funders %}
<div class="section-card">

<h4>Funding</h4>

<div
  class="sponsor-logos"
  style="
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    gap: var(--space-6);
  ">

{% for funder in site.data.funders %}
<a
  href="{{ funder.url }}"
  target="_blank"
  rel="noopener noreferrer">

  <img
    src="{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}"
    alt="{{ funder.name_en | default: funder.name | default: 'Funding organization logo' }}"
    style="
      max-height: 80px;
      max-width: 200px;
      border-radius: 0;
    "
    loading="lazy">

</a>
{% endfor %}

</div>
</div>
{% endif %}
{% endcomment %}

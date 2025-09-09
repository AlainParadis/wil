---
layout: default
title: Fieldwork Employers
---
This is a list of {{ site.data.employers.size }} employers who've taken students on Fieldwork in past years. You'll have to do your own research to find out who to contact. 

{% assign modality_groups = site.data.employers | group_by: "Modality" %}

<!-- 
<ul class="none">
{% for group in modality_groups %}
  <li>{{ group.name }}: {{ group.items | size }}</li>
{% endfor %}
</ul>
 -->

<ul class="legend">
  <li data-modality="all" class="active">
    <span>All</span>
  </li>
  <li data-modality="In-Person">
   <img src="{{ site.url }}{{ site.baseurl }}/svg/in-person.svg" alt="In-Person" width="20" height="20">
    <span>In-Person</span>
  </li>
  <li data-modality="Hybrid">
    <img src="{{ site.url }}{{ site.baseurl }}/svg/hybrid.svg" alt="Hybrid" width="20" height="20">
    <span>Hybrid</span>
  </li>
  <li data-modality="Remote">
    <img src="{{ site.url }}{{ site.baseurl }}/svg/remote.svg" alt="Remote" width="20" height="20">
    <span>Remote</span>
  </li>
</ul>

<ul class="employers">
  {% for row in site.data.employers %}
  <li>
    <strong>
      <a href="{{ row.URL }}" target="_blank" class="{% if row.Hired %}crossed-out{% endif %}">{{ row.Employer }}</a>
    </strong>, 
    <span><a href="mailto:{{ row['E-mail'] }}">{{ row.Contact }}</a></span>, 
    <span>{{ row.Location }}</span>, 
    <span>
      {% if row.Modality == "In-Person" %}
        <img src="{{ site.url }}{{ site.baseurl }}/svg/in-person.svg" alt="In-Person" width="20" height="20">
      {% elsif row.Modality == "Hybrid" %}
        <img src="{{ site.url }}{{ site.baseurl }}/svg/hybrid.svg" alt="Hybrid" width="20" height="20">
      {% elsif row.Modality == "Remote" %}
        <img src="{{ site.url }}{{ site.baseurl }}/svg/remote.svg" alt="Remote" width="20" height="20">
      {% else %}
        {{ row.Modality }}
      {% endif %}
    </span>
  </li>
  {% endfor %}
</ul>



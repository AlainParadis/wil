---
layout: default
title: Fieldwork Employers
---
This is a list of employers who've taken students on Fieldwork in past years. You'll have to do your own research to find out who to contact.

<ul class="legend">
  <li>
    <img src="/svg/in-person.svg" alt="In-Person" width="20" height="20">
    <span>In-Person</span>
  </li>
  <li>
    <img src="/svg/hybrid.svg" alt="Hybrid" width="20" height="20">
    <span>Hybrid</span>
  </li>
  <li>
    <img src="/svg/remote.svg" alt="Remote" width="20" height="20">
    <span>Remote</span>
  </li>
</ul>


<ul class="employers">
  {% for row in site.data.employers %}
  <li>
    <strong><a href="{{ row.URL }}" target="_blank">{{ row.Employer }}</a></strong>, 
    <span><a href="mailto:{{ row['E-mail'] }}">{{ row.Contact }}</a></span>, 
    <span>{{ row.Location }}</span>, 
    <span>
      {% if row.Modality == "In-Person" %}
        <img src="/svg/in-person.svg" alt="In-Person" width="20" height="20">
      {% elsif row.Modality == "Hybrid" %}
        <img src="/svg/hybrid.svg" alt="Hybrid" width="20" height="20">
      {% elsif row.Modality == "Remote" %}
        <img src="/svg/remote.svg" alt="Remote" width="20" height="20">
      {% else %}
        {{ row.Modality }} <!-- Fallback to text if no match -->
      {% endif %}
    </span>
  </li>
  <hr>
  {% endfor %}
</ul>


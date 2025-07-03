---
layout: default
title: Home
---

{{ site.data.course-info.course-description }}

### [Portfolio Development](portfolio-development.html)

This unofficial summer activity is designed to help you kickstart your professional network to gain valuable insights for building your portfolio. By reaching out to [professional designers](employers.html), you'll receive expert advice on your current work and guidance for your future career in graphic design. [Read more…](portfolio-development.html)

### <a name="grads">Grad Web Sites</a>

We have grad web sites for each year. You can find them here:

<div class="grad-site-list">
2025, <a href="https://2025.grads.algonquindesign.ca">Kaleido</a><br>
2024, <a href="https://2024.grads.algonquindesign.ca">Zenith</a><br>
2023, <a href="https://2023.grads.algonquindesign.ca">Resolve</a><br>
2022, Collation<br>
2021, <a href="https://2021.grads.algonquindesign.ca">Generation Adaptation</a><br>
2020, <a href="https://2020.grads.algonquindesign.ca">Anthology</a><br>
2019, <a href="https://2019.grads.algonquindesign.ca">Pathfinder</a><br>
2018, <a href="http://2018.grads.algonquindesign.ca">Reboot</a><br>
2017, <a href="https://2017.grads.algonquindesign.ca">Studio N</a><br>
2016, <a href="https://2016.grads.algonquindesign.ca">Framework</a><br>
2015, <a href="https://2015.grads.algonquindesign.ca">Multiply</a><br>
2014, <a href="https://2014.grads.algonquindesign.ca">Level 14</a><br>
2013, <a href="https://2013.grads.algonquindesign.ca">Grad Show</a><br>
2012, <a href="https://2012.grads.algonquindesign.ca">Grads 2012</a><br>
</div>
 
### I Got Fieldwork!

These are the students who have fieldwork and where they're going.

{% assign fieldwork_count = site.data.i-got-fieldwork | size %}

<p class="mono center"><em>{{ fieldwork_count }}</em> of <em>{{ site.total_students }}</em> students have fieldwork.</p>

<table>
  <thead>
    <tr>
      <th>First</th>
      <th>Last</th>
      <th>Organization</th>
    </tr>
  </thead>
  <tbody>
    {% for student in site.data.i-got-fieldwork %}
    <tr>
      <td>{{ student.first_name }}</td>
      <td>{{ student.last_name }}</td>
      <td><a href="{{ student.studio_url }}">{{ student.studio_name }}</a></td>
    </tr>
    {% endfor %}
  </tbody>
</table>


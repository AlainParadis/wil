---
layout: default
title: Home
---

{{ site.data.course-info.course-description }}

### [Portfolio Development](portfolio-development.html)

This unofficial summer activity is designed to help you kickstart your professional network to gain valuable insights for building your portfolio. By reaching out to [professional designers](employers.html), you'll receive expert advice on your current work and guidance for your future career in graphic design. [Read more…](portfolio-development.html)

### <a name="grads">Grad Web Sites</a>

We have grad web sites for each year. You can find them here:

2025, [Kaleido](https://2025.grads.algonquindesign.ca)  
2024, [Zenith](https://2024.grads.algonquindesign.ca)  
2023, [Resolve](https://2023.grads.algonquindesign.ca)  
<!-- 2022, [Collation](https://2022.grads.algonquindesign.ca)   -->
2021, [Generation Adaptation](https://2021.grads.algonquindesign.ca)  
2020, [Anthology](https://2020.grads.algonquindesign.ca)  
2019, [Pathfinder](https://2019.grads.algonquindesign.ca)  
2018, [Reboot](http://2018.grads.algonquindesign.ca)  
2017, [Studio N](https://2017.grads.algonquindesign.ca)  
2016, [Framework](https://2016.grads.algonquindesign.ca)  
2015, [Multiply](https://2015.grads.algonquindesign.ca)  
2014, [Level 14](https://2014.grads.algonquindesign.ca)  
2013, [Grad Show](https://2013.grads.algonquindesign.ca)  
2012, [Grads 2012](https://2012.grads.algonquindesign.ca)  
 
### I Got Fieldwork!

These are the students who have fieldwork and where they got it.

{% assign fieldwork_count = site.data.i-got-fieldwork | size %}

<p>{{ fieldwork_count }} of {{ site.total_students }} students have fieldwork.</p>

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


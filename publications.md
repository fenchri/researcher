---
layout: page  
title: publications  
index: 1  
permalink: /publications/  
sections: [2022, 2021, 2019, 2018, 2016]
theses: [Theses]
nav: true
---

You can also check my [Google Scholar](https://scholar.google.co.uk/citations?user=nVKZdJkAAAAJ&hl=en&authuser=1) page.

<div class="publications">

{% for y in page.sections %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

{% for y in page.theses %}
  <h2 class="theses">{{y}}</h2>
  {% bibliography -f papers -q @*[section={{y}}]* %}
{% endfor %}

</div>
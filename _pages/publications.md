---
layout: page
permalink: /publications/
title: publications
description: 
years: [2020,2021,2022]
---

{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

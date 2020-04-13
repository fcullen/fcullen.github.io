---
layout: page
permalink: /publications/
title: publications
description: 
years: [2020, 2019, 2018, 2017, 2016, 2014]
---

Below is a list of my first author publications. A full ADS query for all my publications can be found [here](https://ui.adsabs.harvard.edu/search/q=%20%20author%3A%22Cullen%2C%20Fergus%22%20year%3A2014-&sort=date%20desc%2C%20bibcode%20desc&p_=0)

{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

---
layout: page
title: projects
permalink: /projects/
description: Currently active research projects.
---

{% for project in site.projects %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">    
        <span><p><font color="#53744E"><strong>{{ project.title }}</strong></font>: <font color="#666" size="2">{{ project.description }}</font></p></span>
        </a>
</div>

{% endif %}

{% endfor %}

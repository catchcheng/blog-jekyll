---
layout: page
title: Project
permalink: /docs/
---

# Project

Welcome to the {{ site.title }} project pages! Here you can quickly jump to a
particular page.

<div class="section-index">
    <hr class="panel-line">
    {% for post in site.docs  %}        
    <div class="entry">
    <h5><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h5>
    <p>{{ post.description }}</p>
    </div>{% endfor %}
</div>

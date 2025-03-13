---
layout: dark
title: About
example: "Example text in this varible."
---

This is an example of About page in minima theme from Jekyll.  
This page describes the amazing {{ site.title }} by {{ site.author.name }}.

{{ page.example }}

{% include big-cat.html %}

{% for animal in site.data.animal %}
- The {{ animal.name }} is a {{ animal.size }} animal
{% endfor %}

## Large animal are the best!

{% for animal in site.data.animal %}
{% if animal.size == "large" %} - <strong style="color: {{ animal.color }};">{{ animal.name }}</strong>

{% else %} - <small>{{ animal.name }}</small>
{% endif %}
{% endfor %}

# Using where filter
{% assign small_animal = site.data.animal | where: "size", "small" %}
{% for animal in small_animal %}
{{ animal.name | upcase }}
{% endfor %}

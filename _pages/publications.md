---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

#### You can also find my articles on [my Google Scholar profile](https://scholar.google.com/citations?user=HeACvaEAAAAJ&hl=en)

{% include base_path %}

## Main Conference Proceedings 

{% for post in site.main_conf reversed %}
  {% include archive-single.html %}
{% endfor %}

## Workshop Papers

{% for post in site.workshops reversed %}
  {% include archive-single.html %}
{% endfor %}

## Reports

{% for post in site.reports reversed %}
  {% include archive-single.html %}
{% endfor %}

## Popular Science 

{% for post in site.pop reversed %}
  {% include archive-single.html %}
{% endfor %}

## Opinion

{% for post in site.opin reversed %}
  	{% include archive-single.html %}
{% endfor %}


---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

## You can also find my articles on [my Google Scholar profile](https://scholar.google.com/citations?user=HeACvaEAAAAJ&hl=en)

{% include base_path %}

## Main Conference Proceedings 

{% for post in site.collection.main_conf reversed %}
  {% include archive-single.html %}
{% endfor %}

## Workshop Papers

{% for post in site.collection.workshops reversed %}
  {% include archive-single.html %}
{% endfor %}

## Reports

{% for post in site.publications.reports reversed %}
  {% include archive-single.html %}
{% endfor %}

## Popular Science 

{% for post in site.publications.pop reversed %}
  {% include archive-single.html %}
{% endfor %}

## Opinion

{% for post in site.categories.opin reversed %}
  {% include archive-single.html %}
{% endfor %}


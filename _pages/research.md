---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

## Job Market Paper

{% for post in site.jmp reversed %}
  {% include archive-single.html %}
{% endfor %}

## Other Working Papers

{% for post in site.working-papers reversed %}
  {% include archive-single.html %}
{% endfor %}

## Works in Progress

{% for post in site.in-progress reversed %}
  {% include archive-single.html %}
{% endfor %}

## Publications

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
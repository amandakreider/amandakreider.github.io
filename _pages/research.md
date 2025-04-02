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

## Publications in Economics

{% for post in site.pubsecon reversed %}
  {% include archive-single.html %}
{% endfor %}

## Publications in Health Policy, HSR, and Medicine

{% for post in site.pubsmed reversed %}
  {% include archive-single.html %}
{% endfor %}
---
layout: archive
title: "Side Projects"
permalink: /side-projects/
author_profile: true
---

{% include base_path %}

{% for post in site.side-projects reversed %}
  {% include archive-single.html %}
{% endfor %}
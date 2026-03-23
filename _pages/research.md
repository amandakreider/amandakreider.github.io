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

## Working Papers

{% for post in site.working-papers reversed %}
[{{ post.title }}]({{ base_path }}{{ post.url }}){% if post.coauthors %}, with {{ post.coauthors }}{% endif %}

{% endfor %}

## Publications in Economics

{% for post in site.pubsecon reversed %}
{% if post.paperurl and post.paperurl != '' %}[{{ post.title }}]({{ post.paperurl }}){% else %}[{{ post.title }}]({{ base_path }}{{ post.url }}){% endif %}{% if post.coauthors %}, with {{ post.coauthors }}{% endif %}, *{{ post.venue }}*, {{ post.date | date: "%Y" }}

{% endfor %}

## Publications in Health Policy, HSR, and Medicine

{% for post in site.pubsmed reversed %}
{% if post.paperurl and post.paperurl != '' %}[{{ post.title }}]({{ post.paperurl }}){% else %}[{{ post.title }}]({{ base_path }}{{ post.url }}){% endif %}{% if post.coauthors %}, with {{ post.coauthors }}{% endif %}, *{{ post.venue }}*, {{ post.date | date: "%Y" }}

{% endfor %}
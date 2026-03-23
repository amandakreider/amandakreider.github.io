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

## Works in Progress

{% for project in site.data.in-progress %}
{{ project.title }}{% if project.coauthors %}, with {{ project.coauthors }}{% endif %}

{% endfor %}

## Publications in Economics

{% for post in site.pubsecon reversed %}
[{{ post.title }}]({{ base_path }}{{ post.url }}){% if post.coauthors %}, with {{ post.coauthors }}{% endif %}, *{{ post.venue }}*, {{ post.date | date: "%Y" }}

{% endfor %}

## Publications in Health Policy, Health Services Research, and Medicine

{% for post in site.pubsmed reversed %}
[{{ post.title }}]({{ base_path }}{{ post.url }}){% if post.coauthors %}, with {{ post.coauthors }}{% endif %}, *{{ post.venue }}*, {{ post.date | date: "%Y" }}

{% endfor %}

## Publications in Demography (Undergraduate RA Work)

{% for post in site.pubsdem reversed %}
[{{ post.title }}]({{ base_path }}{{ post.url }}){% if post.coauthors %}, with {{ post.coauthors }}{% endif %}, *{{ post.venue }}*, {{ post.date | date: "%Y" }}

{% endfor %}
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
  {% if post.link %}
<p><a href="{{ post.link }}">{{ post.title }}</a></p>
  {% else %}
<p><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a></p>
  {% endif %}
{% endfor %}

## Publications in Economics

{% for post in site.pubsecon reversed %}
{% assign raw_authors = post.citation | split: '. "' | first %}
{% assign author_list = raw_authors | remove: "Kreider, Amanda R.," | remove: "Kreider, Amanda," | remove: ", Amanda R. Kreider" | remove: ", Amanda Kreider" | strip %}
{% if author_list != "" %}
[{{ post.title }}]({{ post.paperurl }}), with {{ author_list }}, *{{ post.venue }}*, {{ post.date | date: "%Y" }}
{% else %}
[{{ post.title }}]({{ post.paperurl }}), *{{ post.venue }}*, {{ post.date | date: "%Y" }}
{% endif %}

{% endfor %}

## Publications in Health Policy, HSR, and Medicine

{% for post in site.pubsmed reversed %}
{% assign raw_authors = post.citation | split: '. "' | first %}
{% assign author_list = raw_authors | remove: "Kreider, Amanda R.," | remove: "Kreider, Amanda," | remove: ", Amanda R. Kreider" | remove: ", Amanda Kreider" | strip %}
{% if author_list != "" %}
[{{ post.title }}]({{ post.paperurl }}), with {{ author_list }}, *{{ post.venue }}*, {{ post.date | date: "%Y" }}
{% else %}
[{{ post.title }}]({{ post.paperurl }}), *{{ post.venue }}*, {{ post.date | date: "%Y" }}
{% endif %}

{% endfor %}
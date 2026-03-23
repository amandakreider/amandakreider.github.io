---
layout: archive
title: "In the Media"
permalink: /media/
author_profile: true
---

{% include base_path %}

## Opinion
{% assign opinion = site.data.media | where: "type", "opinion" %}
{% for item in opinion %}
  <p><a href="{{ item.url }}">{{ item.title }}</a>, <em>{{ item.outlet }}</em>{% if item.author %}, {{ item.author }}{% endif %}, {{ item.date }}</p>
{% endfor %}

## Media Coverage
{% assign coverage = site.data.media | where: "type", "news" %}
{% for item in coverage %}
  <p><a href="{{ item.url }}">{{ item.title }}</a>, <em>{{ item.outlet }}</em>{% if item.author %}, {{ item.author }}{% endif %}, {{ item.date }}</p>
{% endfor %}

## Blog Posts
{% assign blog = site.data.media | where: "type", "blog" %}
{% for item in blog %}
  <p><a href="{{ item.url }}">{{ item.title }}</a>, <em>{{ item.outlet }}</em>{% if item.author %}, {{ item.author }}{% endif %}, {{ item.date }}</p>
{% endfor %}
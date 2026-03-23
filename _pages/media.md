---
layout: archive
title: "In the Media"
permalink: /media/
author_profile: true
---

{% include base_path %}

## Opinion
{% assign opinion = site.data.media | where: "type", "opinion" %}
{% assign opinion = site.data.media | where: "type", "opinion" | sort: "date" | reverse %}
{% for item in opinion %}
  <p><a href="{{ item.url }}">{{ item.title }}</a>, <em>{{ item.outlet }}</em>{% if item.author %}, {{ item.author }}{% endif %}, {{ item.date }}</p>
{% endfor %}

## Media Coverage
{% assign coverage = site.data.media | where: "type", "news" | sort: "date" | reverse %}
{% for item in coverage %}
  <p><a href="{{ item.url }}">{{ item.title }}</a>, <em>{{ item.outlet }}</em>{% if item.author %}, {{ item.author }}{% endif %}, {{ item.date }}</p>
{% endfor %}

## Blog Posts
{% assign blog-external = site.data.media | where: "type", "blog-external" | sort: "date" | reverse %}
{% for item in blog-external %}
  <p><a href="{{ item.url }}">{{ item.title }}</a>, <em>{{ item.outlet }}</em>{% if item.author %}, {{ item.author }}{% endif %}, {{ item.date }}</p>
{% endfor %}

## Blog Posts (Internal)
{% assign blog = site.data.media | where: "type", "blog" | sort: "date" | reverse %}
{% for item in blog %}
  <p><a href="{{ item.url }}">{{ item.title }}</a>, <em>{{ item.outlet }}</em>{% if item.author %}, {{ item.author }}{% endif %}, {{ item.date }}</p>
{% endfor %}


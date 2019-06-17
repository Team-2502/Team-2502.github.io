---
layout: page
title: Scouting Index
permalink: /scouting
---

These are all the wiki pages related to scouting

{% assign groups = site.strategy | group_by: "category" | sort: "name" %}
{% for group in groups %}
{% if group.name != "" %}
#### {{ group.name}}
{% else %}
{% if group.items %}
#### General
{%endif%}
{% else %}
{%endif%}
{% for item in group.items %}
[{{ item.title }}]({{ item.url }})
{%endfor%}
{%endfor%}

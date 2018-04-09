---
layout: page
title: Build Index
permalink: /build
---

These are all the wiki pages related to the fabrication and design of the robot, more colloquially known as "build stuff".

{% assign groups = site.build | group_by: "category" | sort: "name" %}
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

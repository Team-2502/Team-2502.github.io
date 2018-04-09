---
layout: post
title: Programming Index
permalink: /programming
---

These are all the wiki pages related to programming.

{% assign groups = site.programming | group_by: "category" | sort: "name" %}
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

---
title: "Blogg"
slug: blogg
original_url: https://bruk2fa.no/blogg/
date: 2020-09-18T23:11:44
modified: 2020-09-18T23:11:44
layout: page
permalink: /blogg/
---

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: "%d.%m.%Y" }}
{% endfor %}

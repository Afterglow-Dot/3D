---
title: 学习笔记
icon: fas fa-book
order: 2
permalink: /notes/
---

{% for post in site.notes.docs reversed %}
## [{{ post.title }}]({{ post.url | relative_url }})

{{ post.description }}

📅 {{ post.date | date: "%Y-%m-%d" }}

---
{% endfor %}
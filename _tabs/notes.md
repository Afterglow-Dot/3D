---
title: 学习笔记
icon: fas fa-book
order: 2
permalink: /notes/
---

{% if site.notes.size == 0 %}
正在建设中，敬请期待。
{% else %}
{% for post in site.notes reversed %}
## [{{ post.title }}]({{ post.url | relative_url }})

{{ post.description }}

📅 {{ post.date | date: "%Y-%m-%d" }}

---
{% endfor %}
{% endif %}
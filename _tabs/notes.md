---
title: 学习笔记
icon: fas fa-book
order: 2
permalink: /notes/
---
正在建设中，敬请期待。

{% for post in site.notes reversed %}
## [{{ post.title }}]({{ post.url | relative_url }})

{{ post.description }}

📅 {{ post.date | date: "%Y-%m-%d" }}

---
{% endfor %}
---
title: 科研进展
icon: fas fa-flask
order: 3
permalink: /research/
---
{% if site.research.size == 0 %}
正在建设中，敬请期待。
{% else %}
{% for post in site.research reversed %}
## [{{ post.title }}]({{ post.url | relative_url }})

{{ post.description }}

📅 {{ post.date | date: "%Y-%m-%d" }}

---
{% endfor %}
{% endif %}
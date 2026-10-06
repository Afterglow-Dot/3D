---
title: 日常记录
icon: fas fa-coffee
order: 5
permalink: /life/
---

{% if site.life.size == 0 %}
正在建设中，敬请期待。
{% else %}
{% for post in site.life reversed %}
## [{{ post.title }}]({{ post.url | relative_url }})

{{ post.description }}

📅 {{ post.date | date: "%Y-%m-%d" }}

---
{% endfor %}
{% endif %}
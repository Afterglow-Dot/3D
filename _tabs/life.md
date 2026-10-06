---
title: 日常记录
icon: fas fa-coffee
order: 5
permalink: /life/
---

{% for post in site.life reversed %}
## [{{ post.title }}]({{ post.url | relative_url }})

{{ post.description }}

📅 {{ post.date | date: "%Y-%m-%d" }}

---
{% endfor %}
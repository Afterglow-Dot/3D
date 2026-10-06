---
title: 日常记录
icon: fas fa-coffee
order: 5
---

{% for post in site.life.docs reversed %}
## [{{ post.title }}]({{ post.url | relative_url }})

{{ post.description }}

📅 {{ post.date | date: "%Y-%m-%d" }}

---
{% endfor %}
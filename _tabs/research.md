---
title: 科研进展
icon: fas fa-flask
order: 3
permalink: /research/
---

{% for post in site.research.docs reversed %}
## [{{ post.title }}]({{ post.url | relative_url }})

{{ post.description }}

📅 {{ post.date | date: "%Y-%m-%d" }}

---
{% endfor %}
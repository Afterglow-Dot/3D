---
title: 学术成果
icon: fas fa-file-alt
order: 4
permalink: /publications/
---

{% if site.publications.size == 0 %}
正在建设中，敬请期待。
{% else %}
{% for post in site.publications reversed %}
## [{{ post.title }}]({{ post.url | relative_url }})

{{ post.description }}

📅 {{ post.date | date: "%Y-%m-%d" }}

---
{% endfor %}
{% endif %}
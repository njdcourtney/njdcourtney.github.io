---
layout: default
title: Nathan's Blog
---

##Recent posts:

{% for post in site.posts %}
### [ {{ post.title }} ]( {{ post.url }} )
{{ post.excerpt }} [(more)]({{ post.url }})
{% endfor %}

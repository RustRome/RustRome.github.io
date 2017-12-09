extends: default.liquid
---

{% for post in posts %}
#### [{{ post.title }}]({{ post.path }})
{% assign sc = post.content|split:'.'  %}
{% for start in sc limit:1 %}
{{start}}
{% endfor %}
{% endfor %}

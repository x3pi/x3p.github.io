---
layout: post
permalink:  "/cs/flutter"
active: "cs"
---

<div class="view_year">
{% assign sorted_pages = site.cs  | sort:"order" |reverse %}
{% for cs in sorted_pages %}

{% assign beatles = cs.url | split: "/" %}

{% for member in beatles %}
{% if forloop.index0 == 2 %}
{% if member == "flutter" %}

<div class="materials-item">
    <div class="tt">
      <a href="{{ cs.url }}">{{ cs.title }}</a>
    </div>
    <div class="kw">

      {% for tag in cs.tags  %}

      <a>{{tag}}</a>

      {% endfor %}

    </div>
</div>
{% break %}
{% endif %}
{% endif %}
{% endfor %}
{% endfor %}
</div>
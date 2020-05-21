---
layout: post
permalink:  "/cs/ai"
active: "cs"
---

<div class="view_year">
{% assign sorted_pages = site.cs  | sort:"order" | reverse %}
{% for cs in sorted_pages %}

{% assign beatles = cs.url | split: "/" %}

{% for member in beatles %}
{% if forloop.index0 == 2 %}
{% if member == "ai" %}
{% if cs.permalink != "/cs/ai" %}


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
{% endif %}
{% break %}
{% endif %}
{% endif %}
{% endfor %}
{% endfor %}
</div>
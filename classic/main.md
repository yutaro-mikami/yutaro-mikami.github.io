---
layout: hobby
title: 好きなクラシック曲
permalink: /classic/main.html
back: /hidden.html
unlisted: true
---
好きなクラシックの名盤のまとめ．

ミーハーな素人が書いたものであると理解した上で見てください．

<ul>
{% assign reviews = site.music_reviews | sort: "order" %}
{% for item in reviews %}
  {% if item.listed != false %}<li><a href="{{ item.url | relative_url }}">{{ item.link_title }}</a></li>{% endif %}
{% endfor %}
</ul>

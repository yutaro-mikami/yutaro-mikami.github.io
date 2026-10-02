---
layout: hobby
title: 非公式のもの
theme: hidden
permalink: /hidden.html
back: /index_jp.html
unlisted: true
---

## 論文についてのコメント

ここでは自分の論文についてのコメントなどを書いている．タイトル後の括弧の中身は文章の作成時期である．

<ul>
{% assign comments = site.paper_comments | sort: "order" %}
{% for item in comments %}
  {% if item.listed != false %}<li><a href="{{ item.url | relative_url }}">{{ item.link_title }}</a></li>{% endif %}
{% endfor %}
</ul>

## どうでも良い話

- [好きなクラシック曲]({{ '/classic/main.html' | relative_url }})
- [好きなアニメ，漫画，ラノベなど]({{ '/anime/main.html' | relative_url }})

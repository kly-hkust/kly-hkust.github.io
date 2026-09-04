---
title: "News"
layout: textlay
excerpt: "News: KLY Group @ HKUST."
permalink: /allnews.html
---

# News

<div class="well">
{% for article in site.data.news %}
<p>{{ article.date }}<br/>
{{ article.headline}}</p>
{% endfor %}
</div>

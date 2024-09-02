---
title: "KLY Lab - Pictures"
layout: piclay
excerpt: "KLY Lab -- Pictures"
permalink: /pictures/
---

# Pictures

## HKUST

#### Videos
<iframe width="280" height="160" src="https://www.youtube.com/embed/0zSOYfwt2cw" frameborder="0" allowfullscreen></iframe>
<iframe width="280" height="160" src="https://www.facebook.com/watch/?v=232757281238342" frameborder="0" allowfullscreen></iframe>

#### Gallery
(Right-click *'view image'* to see a larger image.)
{% assign number_printed = 0 %}
{% for pic in site.data.pictures_ust %}

{% assign even_odd = number_printed | modulo: 4 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-3 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/inst/{{ pic.image }}" class="img-responsive" width="95%" style="float: left" />
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd > 2 %}
</div>
{% endif %}


{% endfor %}

{% assign even_odd = number_printed | modulo: 4 %}
{% if even_odd == 1 %}
</div>
{% endif %}

{% if even_odd == 2 %}
</div>
{% endif %}

{% if even_odd == 3 %}
</div>
{% endif %}

<p> &nbsp; </p>
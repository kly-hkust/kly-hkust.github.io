---
title: "KLY Group - Team"
layout: gridlay
excerpt: "KLY Group: Team members"
permalink: /team/
---

# Group Members

**We are looking for motivated PhD and Master's students and postdoctoral researchers to join our team.**


Jump to [Staff](#staff), [Current Students](#current-students), or [Alumni](#alumni).

## Principal Investigator
{% assign number_printed = 0 %}
{% for member in site.data.team_pi %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/optimized/teampic/{{ member.photo }}.webp" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <span>{{ member.info0 }} <br>{{ member.info1 }} <br>{{ member.info2 }}</span>
  <p class="pi-contact">[ <a href="mailto:{{ member.email }}">{{ member.email }}</a> | <a href="tel:+85223587123" title="+852 2358 7123">2358 7123</a> | <a href="https://pathadvisor.ust.hk/search/nearest/lift/from/4550" target="_blank" rel="noopener">Room 4550</a> ]</p>
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 | markdownify}} </li>
  <li> {{ member.education2 | markdownify}} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

  {% if member.number_educ == 6 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  <li> {{ member.education6 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Staff
{% assign number_printed = 0 %}
{% for member in site.data.team_staff %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/optimized/teampic/{{ member.photo }}.webp" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  {% if member.phone %}
  <span>{{ member.info0 }} <br>{{ member.info1 }}</span>
  <p class="pi-contact">[ <a href="mailto:{{ member.email }}">{{ member.email }}</a> | <a href="tel:{{ member.phone_link }}" title="{{ member.phone_link }}">{{ member.phone }}</a> | <a href="{{ member.office_url }}" target="_blank" rel="noopener">{{ member.office }}</a> ]</p>
  {% else %}
  <span>{{ member.info0 }} <br>{{ member.info1 }} <br>email: <a href="mailto:{{ member.email }}">{{ member.email }}</a></span>
  {% endif %}
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 | markdownify}} </li>
  <li> {{ member.education2 | markdownify}} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Current Students
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/optimized/teampic/{{ member.photo }}.webp" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <span>{{ member.info0 }} <br>email: <{{ member.email }}></span>
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 | markdownify}} </li>
  <li> {{ member.education2 | markdownify}} </li>
  {% endif %}

  </ul>
</div>


{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


<!-- ## Alumni

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/optimized/teampic/{{ member.photo }}.webp" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <span>{{ member.duration }} <br> Role: {{ member.info }}</span>
  <ul style="overflow: hidden">

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %} -->

## Alumni
<div class="row">

<div class="col-sm-4 clearfix">
<h4>Postdoc</h4>
{% for member in site.data.alumni_postdoc %}
{{ member.name }}<br><span>{{ member.info0 }} </span><br><span>{{ member.info1 }} </span>
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>PhD Graduates</h4>
{% for member in site.data.alumni_phd %}
{{ member.name }}<br><span>{{ member.info0 }} </span>
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Master Graduates</h4>
{% for member in site.data.alumni_ms %}
{{ member.name }}<br><span>{{ member.info0 }} </span>
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Staff</h4>
{% for member in site.data.alumni_staff %}
{{ member.name }}<br><span>{{ member.info0 }} </span>
{% endfor %}
</div>

</div>


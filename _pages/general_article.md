---
title: "Hydro90 - Article"
layout: pagelay
excerpt: "Hydro90 -- Article."
sitemap: false
permalink: /general_article/
---


# 论文速递
### 2020.06-2021.04
{% assign number_printed = 0 %}
{% for member in site.data.general_article %}

<div class="col-sm-12 clearfix">
  <h4>  <a href="{{ member.url }}"> {{member.no}} - {{ member.title }} </h4>
   <i> <b> {{ member.name }} </b>({{ member.info }}), {{ member.email }},</i> <i> ({{ member.date }})</i>
</div>

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
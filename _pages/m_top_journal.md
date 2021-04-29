---
title: "Hydro90 - 聚焦顶刊"
layout: pagelay
excerpt: "Hydro90 -- Top Journal."
sitemap: false
permalink: /m_top_journal/
---


# 聚焦顶刊
### 2020.09-2021.04
{% assign number_printed = 0 %}
{% for member in site.data.top_journal %}

{% if member.no == "0" %}
<div class="col-sm-12 clearfix">
  <p> <b> <a href="{{ member.url }}">  {{ member.title }} ({{ member.date }}) </a> </b> </p>
</div>
{% else %}
<div class="col-sm-12 clearfix">
  <p>  &nbsp;&nbsp;&nbsp;&nbsp; {{ member.mark }}  {{ member.title }} <i> <a href="{{ member.url }}"> ({{ member.journal }} , {{ member.date }}) </a> </i> </p>
</div>
{% endif %}
{% endfor %}

<p> * 代表该论文被当期聚焦顶刊解读（2020年12月之后每期只解读两篇文章） </p>

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
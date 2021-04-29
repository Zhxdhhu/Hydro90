---
title: "Hydro90 - Team"
layout: pagelay
excerpt: "Hydro90 Team members"
sitemap: false
permalink: /team/
---

# 团队成员

 **我们每三月将召集新一期志愿者，共同运营Hydro90，服务读者，敬请留意公众号通知!**

## 编委组


{% assign number_printed = 0 %}

{% for member in site.data.team_member %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }} : {{ member.native }} </h4>
  <i>(ID.{{ member.no }}) {{ member.duration }} <br> {{ member.info }} <br>mail: {{ member.email }} </i>

<ul style="overflow: hidden">

  {% if member.number_desc == "1" %}
  <li> {{ member.description1 }} </li>
  {% endif %}

  {% if member.number_desc == "2" %}
  <li> {{ member.description1 }} </li>
  <li> 研究方向：{{ member.description2 }} </li>
  {% endif %}

  {% if member.number_desc == "3" %}
  <li> {{ member.description1 }} </li>
  <li> 研究方向：{{ member.description2 }} </li>
  <li> {{ member.description3 }} </li>
  {% endif %}

  {% if member.number_desc == "4" %}
  <li> {{ member.description1 }} </li>
  <li> 研究方向：{{ member.description2 }} </li>
  <li> {{ member.description3 }} </li>
  <li> {{ member.description4 }} </li>
  {% endif %}

  {% if member.number_desc == "5" %}
  <li> {{ member.description1 }} </li>
  <li> 研究方向：{{ member.description2 }} </li>
  <li> {{ member.description3 }} </li>
  <li> {{ member.description4 }} </li>
  <li> {{ member.description5 }} </li>
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


## 顾问

{% assign number_printed = 0 %}
{% for member in site.data.team_collaborator %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <h4>{{ member.name }} : {{ member.native }}</h4>
  <i> {{ member.info }}</i>
  <ul style="overflow: hidden">

  {% if member.number_desc == "1" %}
  <li> {{ member.description1 }} </li>
  {% endif %}

  {% if member.number_desc == "2" %}
  <li> {{ member.description1 }} </li>
  <li> 研究方向：{{ member.description2 }} </li>
  {% endif %}

  {% if member.number_desc == "3" %}
  <li> {{ member.description1 }} </li>
  <li> 研究方向：{{ member.description2 }} </li>
  <li> {{ member.description3 }} </li>
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

## 往期编辑
<div class="row">

{% for member in site.data.former_student %}
<div class="col-sm-4 clearfix">
{{ member.name }} : (ID.{{ member.no }}){{ member.duration }} <br/> {{ member.info }}
</div>
{% endfor %}

</div>


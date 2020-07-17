---
title: "team"
layout: gridlay
permalink: /team/
description: We are a team of enthusiastic researchers, consisting of faculty members, research associates and PhD students.
nav: true
---

## lab members

<div class="row" style="margin:0px 0 20px 0">
</div>

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign num_in_row = number_printed | modulo: 3 %}

{% if num_in_row == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/img/team/{{ member.photo }}" class="img-responsive"/>
  <div class="caption">
      <span style="font-size:18px;"> {{ member.name }}</span><br><i style="font-size:16px;">{{ member.info }}</i><br>{{ member.research }}
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if num_in_row == 2 %}
</div>
{% endif %}

{% endfor %}

{% if num_in_row <= 1 %}
</div>
{% endif %}

## collaborators

<div class="row" style="margin:0px 0 20px 0">
</div>

{% assign number_printed = 0 %}
{% for member in site.data.collaborators %}

{% assign num_in_row = number_printed | modulo: 3 %}

{% if num_in_row == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/img/collaborators/{{ member.photo }}" class="img-responsive"/>
  <div class="caption">
      <span style="font-size:18px;"> {{ member.name }}</span><br><i style="font-size:16px;">{{ member.info }}</i><br>{{ member.research }}
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if num_in_row == 2 %}
</div>
{% endif %}

{% endfor %}

{% if num_in_row <= 1 %}
</div>
{% endif %}


## alumni
<div class="row" style="margin:0px 0 20px 0">
</div>

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign num_in_row = number_printed | modulo: 3 %}

{% if num_in_row == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/img/alumni/{{ member.photo }}" class="img-responsive"/>
  <div class="caption">
      <span style="font-size:18px;"> {{ member.name }}</span><br><i style="font-size:16px;">{{ member.info }}</i>
  </div>
 </div>

{% assign number_printed = number_printed | plus: 1 %}

{% if num_in_row == 2 %}
</div>
{% endif %}

{% endfor %}

{% if num_in_row <= 2 %}
</div>
{% endif %}

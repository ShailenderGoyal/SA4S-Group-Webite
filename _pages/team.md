---
title: "Allan Lab - Team"
layout: gridlay
excerpt: "Allan Lab: Team members"
sitemap: false
permalink: /team/
---

# Group Members

**We are looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**

Jump to [staff](#staff), [students](#phd-students), [graduated students](#graduated-students), [administrative support](#administrative-support)


## Faculty

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}
{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 0 %}

<div class="row">
{% endif %}
<div class="col-sm-6 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
<h4>{{ member.name }}</h4>
<i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
<ul style="overflow: hidden">
{% if member.number_educ >= 1 %}
<li> {{ member.education1 }} </li>
{% endif %}
{% if member.number_educ >= 2 %}
<li> {{ member.education2 }} </li>
{% endif %}
{% if member.number_educ >= 3 %}
<li> {{ member.education3 }} </li>
{% endif %}
{% if member.number_educ >= 4 %}
<li> {{ member.education4 }} </li>
{% endif %}
{% if member.number_educ == 5 %}
<li> {{ member.education5 }} </li>
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

<!-- Faculty ends here -->


<!-- Students start here -->

{% assign student_groups = "phd, masters, dual, honours" | split: ", " %}
{% assign group_labels = "PhD, Masters, Dual Degree, Honours" | split: ", " %}


{% for i in (0..student_groups.size) %}
{% assign group = student_groups[i] %}
{% assign group_data = site.data.students[group] %}
{% if group_data == nil %}
{% continue %}
{% endif %}

  <h2>{{ group_labels[i] }} Students</h2>

{% assign number_printed = 0 %}
{% for member in site.data.students[group] %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 0 %}
<div class="row">
{% endif %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!-- <br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden">
  {% if member.number_educ >= 1 %}
    <li> {{ member.education1 }} </li>
  {% endif %}
  {% if member.number_educ >= 2 %}
    <li> {{ member.education2 }} </li>
  {% endif %}
  {% if member.number_educ >= 3 %}
    <li> {{ member.education3 }} </li>
  {% endif %}
  {% if member.number_educ >= 4 %}
    <li> {{ member.education4 }} </li>
  {% endif %}
  {% if member.number_educ == 5 %}
    <li> {{ member.education5 }} </li>
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

{% endfor %}



## Graduated students

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}

<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.duration }} <br> Role: {{ member.info }}</i>
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
{% endif %}

<!--
## Former visitors, BSc/ MSc students
<div class="row">
<div class="col-sm-4 clearfix">
<h4>Visitors</h4>
{% for member in site.data.alumni_visitors %}
{{ member.name }}
{% endfor %}
</div>
<div class="col-sm-4 clearfix">
<h4>Master students</h4>
{% for member in site.data.alumni_msc %}
{{ member.name }}
{% endfor %}
</div>
<div class="col-sm-4 clearfix">
<h4>Bachelor Students</h4>
{% for member in site.data.alumni_bsc %}
{{ member.name }}
{% endfor %}
</div>
</div> -->

## Administrative Support

<a href="mailto:serc.admin@iiit.ac.in">Sree Sahithi</a> is helping us (and other groups) with administration.

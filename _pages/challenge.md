---
title: "Challenge"
layout: textlay
excerpt: "Challenge"
sitemap: false
permalink: /challenge/
---

# Challenge yourself

Coming soon !
 
## Challenge tasks

{% assign number_printed = 0 %}
{% for task in site.data.tasks %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if task.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ task.title }}</pubtit>
  <img src="{{ task.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ task.description }}</p>
  <p><em>{{ task.authors }}</em></p>
  <p><strong><a href="{{ task.link.url }}">{{ task.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ task.news1 }}</strong></p>
  <p> {{ task.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

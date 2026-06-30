---
title: "Atomic Photonic Integrated Circuits Laboratory - Research"
layout: gridlay2
excerpt: "Atomic Photonic Integrated Circuits Laboratory -- Research"
sitemap: false
tags: [10001, 10002,10003, 10004, 10005, 10006]
permalink: /research/
---

# Our Research

<div style="text-align: justify;">
<img class="img-responsive" src="{{ site.url }}{{ site.baseurl }}/images/logopic/Innovation_at_nexus.png" style="float: left; width: 400px; margin: 0 15px 10px 0;"/>
Our vision is to develop technologies that enable the miniaturization of atom-based systems into platforms that are scalable, compact, energy-efficient, and robust to unavoidable external perturbations. By engineering reliable, high-performance quantum systems, we aim to access previously unexplored regimes and address pressing challenges in the field, enabling both fundamental scientific discovery and technological advances in quantum computing and precision metrology.
<div style="clear: both;"></div>
<img class="img-responsive" src="{{ site.url }}{{ site.baseurl }}/images/logopic/physics_to_engineering.png" style="float: left; width: 400px; margin: 0 15px 10px 0;"/>
Our work is interdisciplinary, drawing on the fundamental physics of atom–light interactions while leveraging integrated photonics and microelectromechanical systems (MEMS). In our research, we use micro- and nanofabrication techniques for device fabrication and metrology, state-of-the-art laser and electronic control systems, ultra-high-vacuum and cryogenic technologies, packaging methods for integrated microsystems, and numerical as well as theoretical approaches.
<div style="clear: both;"></div>
The technologies we develop have applications that extend beyond quantum systems to, e.g. visible and ultra-violet integrated photonics, co-packaged optics, integrated optical sources and amplifiers.
</div>

[//]: # (For a high-level summary of a selection of our results, see [Research Results](research_results).)

Have a look at a video from one of the leading start-ups in trapped-ion quantum hardware [Quantinuum](https://www.quantinuum.com/) to gain an overview of current research efforts and the state-of-the-art platform in the field.. You can find some of our recent research themes described at the end of this page.

## Trapped-Ion Quantum Hardware Overview
{% include youtubePlayer.html id="6ZIdE9VnvfM" %}





## Selected research themes
{% assign paper_show = true %}


{% assign number_printed = 0 %}
{% for theme-item in site.data.research_themes %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if theme-item.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}
{% if theme-item.long == 1 %}
<div class="col-sm-12 clearfix">
 <div class="well">
 {% if theme-item.hasimage == 1 %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/themepic/{{ theme-item.image }}" class="img-responsive" width="{{ theme-item.width }}" style="float: top"/>
  {% endif %}
  <h3><pubtit>{{ theme-item.title }}</pubtit></h3>
  <p>{{ theme-item.description }}</p>
  <p>Team members: <em>{{ theme-item.authors }}</em></p>
  <p class="text-danger"><strong> {{ theme-item.news1 }}</strong></p>
  <p> {{ theme-item.news2 }}</p>
  <a data-toggle="collapse" href="#{{theme-item.key}}-bib"  class="btn-bib" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false">Selected papers</a>
<div class="collapse" id="{{theme-item.key}}-bib"><div class="well-abs"><div class="publications">
{%- for y in page.tags %}
{%- if y == theme-item.tag -%}
{% bibliography -f apic_publications -q @*[tag={{y}}]* %}
{% endif %}
{% endfor %}
</div></div></div>
 </div>
</div>
</div>
{% else %}
<div class="col-sm-6 clearfix">
 <div class="well">
 {% if theme-item.hasimage == 1 %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/themepic/{{ theme-item.image }}" class="img-responsive" width="{{ theme-item.width }}" style="float: top"/>
  {% endif %}
  <h3><pubtit>{{ theme-item.title }}</pubtit></h3>
  {{ theme-item.description }}
  <p>Team members: <em>{{ theme-item.authors }}</em></p>
  <p class="text-danger"><strong> {{ theme-item.news1 }}</strong></p>
  <p> {{ theme-item.news2 }}</p>
  <a data-toggle="collapse" href="#{{theme-item.key}}-bib"  class="btn-bib" style="text-decoration:none; color:#ebebeb; hover:#ebebeb;" role="button" aria-expanded="false">Selected papers</a>
<div class="collapse" id="{{theme-item.key}}-bib"><div class="well-abs"><div class="publications">
{%- for y in page.tags %}
{%- if y == theme-item.tag or y == theme-item.taga -%}
{% bibliography -f apic_publications -q @*[tag={{y}} || taga={{y}}]]* %}
{% endif %}
{% endfor %}
</div></div></div>
 </div>
</div>
{% assign number_printed = number_printed | plus: 1 %}
{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


[//]: # (**Watermarking schemes for attack detection:**)

### ... and more.

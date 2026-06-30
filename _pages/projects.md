---
title: "Atomic Photonic Integrated Circuits Laboratory - Projects"
layout: textlay
excerpt: "Atomic Photonic Integrated Circuits Laboratory -- Projects."
sitemap: false
permalink: /projects/
---

# Our Funding
We are grateful to the following organizations that generously fund our activities:
- [Indian Institute of Science](https://www.iisc.ac.in/),



<div class="row">

<div class="col-sm-2 clearfix vcenter">
<img src="{{ site.url }}{{ site.baseurl }}/images/logopic/iisc_logo.png" style="width: 125px">

</div>

Their funding supports our work in research, education, and outreach.

### Selected ongoing projects

{% for project in site.data.project %}

{% if project.ongoing == 1 and project.selected == 1 %}
<div class="row">
<div class="well">

#### {{ project.title }} ({{ project.period}})

**Call:** {{project.category}}, *funded by the* {{ project.agency}}

**Awarded to:** {{project.lead}}

**APIC Members:** {{project.member}}

<div class="btn-group">
  <a class="btn-abstract" data-toggle="collapse" href="#{{project.key}}-abs">**Popular Abstract**</a>
  <a class="btn-papers" data-toggle="collapse" href="#{{project.key}}-bib">**Selected papers**</a>
</div>


<div class="collapse" id="{{project.key}}-abs"><div class="well-abs">
{{ project.summary }}
</div></div>

<div class="collapse" id="{{project.key}}-bib"><div class="well-abs"><div class="publications">
{% bibliography -f apic_publications -q @*[grant={{project.key}} || granta={{project.key}} || grantb={{project.key}} || grantc={{project.key}}]* %}
</div></div></div>


</div>
</div>

{% endif %}

{% endfor %}


### Selected past projects

{% for project in site.data.project %}

{% if project.ongoing == 0 and project.selected == 1 %}
<div class="row">
<div class="well">

#### {{ project.title }} ({{ project.period}})

**Call:** {{project.category}}, *funded by the* {{ project.agency}}

**Awarded to:** {{project.lead}}

**APIC Members:** {{project.member}}

<div class="btn-group">
  <a class="btn-abstract" data-toggle="collapse" href="#{{project.key}}-abs">**Popular Abstract**</a>
  <a class="btn-papers" data-toggle="collapse" href="#{{project.key}}-bib">**Selected papers**</a>
</div>


<div class="collapse" id="{{project.key}}-abs"><div class="well-abs">
{{ project.summary }}
</div></div>

<div class="collapse" id="{{project.key}}-bib"><div class="well-abs"><div class="publications">
{% bibliography -f apic_publications -q @*[grant={{project.key}} || granta={{project.key}} || grantb={{project.key}} || grantc={{project.key}}]* %}
</div></div></div>


</div>
</div>

{% endif %}

{% endfor %}


<h4><a href="{{ site.url }}{{ site.baseurl }}/allprojects.html">... see all Projects</a></h4>

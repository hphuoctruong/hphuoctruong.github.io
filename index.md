---
title: Homepage
layout: page
dynamic_title: true
---
{% assign pinned = site.posts | where_exp: "item", "item.pin == true"  %}
{% assign default = site.posts | where_exp: "item", "item.pin != true"  %}
{% assign posts = "" | split: "" %}

<!-- Get pinned posts -->

{% assign offset = paginator.page | minus: 1 | times: paginator.per_page %}
{% assign pinned_num = pinned.size | minus: offset %}

{% if pinned_num > 0 %}
  {% for i in (offset..pinned.size) limit: pinned_num %}
    {% assign posts = posts | push: pinned[i] %}
  {% endfor %}
{% else %}
  {% assign pinned_num = 0 %}
{% endif %}

**Bui Thi Hoa**\
Postdoctoral Researcher

[Curtin University](www.curtin.edu.au)\
[School of Electrical Engineering, Computing, and Mathematical Sciences](https://scieng.curtin.edu.au/schools/electrical-eng-computing-maths/)\
Phone: (+61)-410939728\
Email: bth.hoa92 at gmail, hoa.bui at curtin.edu.au

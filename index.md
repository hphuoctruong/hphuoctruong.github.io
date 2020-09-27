---
title: Homepage
layout: page
---

**Bui Thi Hoa**\
Postdoctoral Researcher

[Curtin University](www.curtin.edu.au)\
[School of Electrical Engineering, Computing, and Mathematical Sciences](https://scieng.curtin.edu.au/schools/electrical-eng-computing-maths/)\
Phone: (+61)-410939728\
Email: bth.hoa92 at gmail, hoa.bui at curtin.edu.au

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


<!-- Get default posts -->

{% assign default_beg = offset | minus: pinned.size %}

{% if default_beg < 0 %}
  {% assign default_beg = 0 %}
{% endif %}

{% assign default_num = paginator.posts | size | minus: pinned_num  %}
{% assign default_end = default_beg | plus: default_num | minus: 1 %}

{% if default_num > 0 %}
  {% for i in (default_beg..default_end) %}
    {% assign posts = posts | push: default[i] %}
  {% endfor %}
{% endif %}


<div id="post-list">

{% for post in posts %}

  <div class="post-preview">
    <div class="d-flex justify-content-between pr-xl-2">
      <h1><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h1>
      {% if post.pin == true %}
        <i class="fas fa-thumbtack fa-fw text-muted mt-1 ml-2 mt-xl-2" data-toggle="tooltip" data-placement="left"
        title="Pinned"></i>
      {% endif %}
    </div>
    <div class="post-content">
      <p>
        {% include no-linenos.html content=post.content %}
        {{ content | markdownify | strip_html | truncate: 200 }}
      </p>
    </div>
  </div> <!-- .post-review -->

{% endfor %}

</div> <!-- #post-list -->

{% if paginator.total_pages > 0 %}
  {% include post-paginator.html %}
{% endif %}

---
layout: page
permalink: /Drug/
title: Drug
---


<div id="archives">
{% for Drug in site.categories %}
  <div class="archive-group">
    {% capture Drug_name %}{{ Drug | first }}{% endcapture %}
    <div id="#{{ Drug_name | slugize }}"></div>
    <p></p>
    <h3 class="Drug-head">{{ Drug_name }}</h3>
    <a name="{{ Drug_name | slugize }}"></a>
    {% for post in site.Drug[Drug_name] %}
    <article class="archive-item">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
    {% endfor %}
  </div>
{% endfor %}
</div>

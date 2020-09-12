
---
layout: posts
permalink: /projects/
title: "Projects"
author_profile: true
header:
  image: "/images/fort point.png"
---
Here are some of the core projects in Artificial Intelligence , Machine Learning , Deep Learning , Computer Vision , Data Structures , Algorithms , Python , Flask , Tensorflow , Pytorch , Keras , Scikit-Learn , OS



{% include base_path %}
{% include group-by-array collection=site.projects field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}

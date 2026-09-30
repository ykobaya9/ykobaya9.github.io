---
permalink: /
title: "About"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a second-year doctoral student advised by [Dr. Shalmali Joshi](https://shalmalijoshi.github.io/reAIM/) at the [Department of Biomedical Informatics](https://www.dbmi.columbia.edu/) at Columbia University. 

## Selected Works

{% include base_path %}
{% for category in site.publication_category %}
{% assign title_shown = false %}
{% for post in site.publications reversed %}
{% if post.category != category[0] %}{% continue %}{% endif %}
{% unless title_shown %}
<h3>{{ category[1].title }}</h3>
{% assign title_shown = true %}
{% endunless %}
{% include archive-single.html title_tag="h4" %}
{% endfor %}
{% endfor %}

---
permalink: /
seo_title: "Yuta Kobayashi | Columbia University"
description: "Yuta Kobayashi is a doctoral student in biomedical informatics at Columbia University, advised by Dr. Shalmali Joshi. His research covers AI reliability and robustness in data-scarce settings, uncertainty, missing data, and cost-efficient data acquisition."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

## About

I am a doctoral student advised by [Dr. Shalmali Joshi](https://shalmalijoshi.github.io/reAIM/) at the [Department of Biomedical Informatics](https://www.dbmi.columbia.edu/) at Columbia University. 

I am interested in developing methods to enhance AI reliability and robustness in data-scarce environments, with a focus on handling uncertainty and missing data. My current research uses principles from causality, Bayesian inference, and reinforcement learning to guide cost-efficient data acquisition under uncertainty.

## Selected Works

{% capture author_bold %}<strong>{{ site.author.name }}</strong>{% endcapture %}
{% for category in site.publication_category %}
{% assign title_shown = false %}
{% for post in site.publications reversed %}
{% if post.category != category[0] %}{% continue %}{% endif %}
{% unless title_shown %}
<h3>{{ category[1].title }}</h3>
{% assign title_shown = true %}
{% endunless %}
<div class="list__item">
<article class="archive__item">
<p>{% if post.paperurl %}<a href="{{ post.paperurl }}"><strong>{{ post.title }}</strong></a>{% else %}<strong>{{ post.title }}</strong>{% endif %}<br />
{{ post.authors | replace: site.author.name, author_bold }}<br />
{% if post.venue %}<i>{{ post.venue }}</i>{% elsif post.status %}<i>{{ post.status }}</i>{% endif %}, {{ post.date | default: "1900-01-01" | date: "%Y" }}</p>
<p class="archive__item-excerpt">{{ post.excerpt | markdownify | remove: '<p>' | remove: '</p>' }}</p>
</article>
</div>
{% endfor %}
{% endfor %}

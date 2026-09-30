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
<p><strong>{{ post.title }}</strong><br />
{{ post.authors | replace: site.author.name, author_bold }}<br />
{% if post.venue %}<i>{{ post.venue }}</i>{% elsif post.status %}<i>{{ post.status }}</i>{% endif %}, {{ post.date | default: "1900-01-01" | date: "%Y" }}{% if post.paperurl %} &middot; <a href="{{ post.paperurl }}">Paper</a>{% endif %}</p>
<p class="archive__item-excerpt">{{ post.excerpt | markdownify | remove: '<p>' | remove: '</p>' }}</p>
</article>
</div>
{% endfor %}
{% endfor %}

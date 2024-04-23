---
layout: page
title: Recent trends
---
<style>
body {
  background-image: url('/public/logo_mda-net.svg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: 15% 15%;
  background-position: 100% 20%;
}
</style>

Contributions are welcome! 

*If you are interested in posting a short announcement, please contact [Diego Ruano](https://www.singacom.uva.es/~ruano/)*.

{% for post in site.posts %}
{% if post.tag=='Trend' %}
### <a href="{{ post.url }}">{{ post.title }}</a>
<span class="post-date">{{ post.date | date_to_string }}</span>
{{post.abstract}} (<a href="{{ post.url }}">read more</a>)
{% endif %}
{% endfor %}


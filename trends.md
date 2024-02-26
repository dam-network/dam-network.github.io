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

{% for post in site.posts reversed %}
{% if post.tag=='Trend' %}
### <a href="{{ post.url }}">{{ post.title }}</a>
{{post.abstract}} (<a href="{{ post.url }}">read more</a>)
{% endif %}
{% endfor %}


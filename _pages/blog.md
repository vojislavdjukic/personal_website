---
layout: main
title: "Blog"
permalink: /blog/
author_profile: true
---

{% include fix/base_path %}

{% for post in site.posts reversed %}
   {% include post-preview.html %}
{% endfor %}

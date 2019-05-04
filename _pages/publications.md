---
layout: main
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% for post in site.publications reversed %}
   {% include publications-preview.html %}
{% endfor %}

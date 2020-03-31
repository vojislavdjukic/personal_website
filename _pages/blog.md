---
layout: main
title: "Blog"
permalink: /blog/
author_profile: true
---

{% include fix/base_path %}

{% assign one_post_exists = false %}

{% for post in site.posts reversed %}
    {% if post.ready %}
        {% assign one_post_exists = true %}
        {% include post-preview.html %}
    {% endif %}
{% endfor %}

{% if one_post_exists == false %}
    {% include empty-blog.html %}
{% endif %}

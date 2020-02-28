---
layout: main
permalink: /
title: ""
excerpt: "PhD candidate doing distributed and networked system research"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a PhD candidate in Network Design & Architecture Lab (<a class="flink" href="https://ndal.ethz.ch/">NDAL</a>), led by <a class="flink" href="https://people.inf.ethz.ch/asingla/">Ankit Singla</a>.
My area of research is computer networks, distributed systems, and cloud computing.

Contact
------
<span class="c_main">vojislav.dukic@inf.ethz.ch</span> <br/>
<small class="c_light_text">Phone: +41 44 632 78 22 <br />
Address: CAB  E71.2, <br />
Universitätstrasse 6, <br />
8006 Zürich <br />
</small>


Research
------

<div class="featured_posts">
{% for post in site.publications reversed %}
  {% include publications-featured.html %}
{% endfor %}
</div>

<div><small><a class="flink" style="font-style: italic;" href="{{ base_path }}/publications">More publications</a></small></div>


Teaching
------
ETH Zurich:<br />
Future Internet (<a class="flink" href="https://ndal.ethz.ch/courses/fi.html">link</a>) - 2019, 2020 <br />
Advanced Computer Networks (<a class="flink" href="https://ndal.ethz.ch/courses/acn.html">link</a>) - 2017, 2018 <br />
Computer Networks (<a class="flink" href="https://ndal.ethz.ch/courses/networks.html">link</a>) - 2019, 2020 <br />

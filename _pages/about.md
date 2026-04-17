---
permalink: /
title: "About Me"
layout: single
author_profile: true
redirect_from: 
  - /about.html
---
<div style="display: flex; align-items: flex-start; gap: 40px;">

<div style="flex: 1;">
I joined Sookmyung Women’s University as an Assistant Professor (Sep. '25). I received my Ph.D. in Computer Engineering from Seoul National University under Prof. <a href="https://scholar.google.com/citations?user=KRykCKkAAAAJ&hl=en">Chong-Kwon Kim</a>. 

My research interests include emerging machine learning algorithms, large language models, graph neural networks, and recommender systems.
</div>

<div style="flex: 1;">
  <img src="/images/photogray.jpg" style="width: 100%; border-radius: 8px;">
</div>

</div>

News
======

<div style="width: 50px; border-bottom: 3px solid #b5894b; margin-bottom: 1em;"></div>

{% for item in site.data.news %}
<p style="margin: 0.3em 0;">[{{ item.date }}] {{ item.text | markdownify | remove: "<p>" | remove: "</p>" }}</p>
{% unless forloop.last %}<hr style="border: none; border-top: 0.5px solid #ccc; margin: 0.6em 0;">{% endunless %}
{% endfor %}




<!--
Work experience
======
* Sep. 2025 ~ : Assistant Professor
  * Sookmyung Women's University, Seoul (Dept. of AI)

* Oct. 2024 ~ Aug. 2025: Research Scientist
  * Samsung SDS, Seoul (AI Preceding Lab)

* Nov. 2023 ~ Sep. 2024: Postdoc
  * Arizona State University, Tempe (School of Computing and Augmented Intelligence)

* Sep. 2023 ~ Nov. 2023: Postdoc
  * Korea Institute of Energy Technology, Naju (Energy AI)

Education
======
* Mar. 2019 ~ Aug. 2023: Seoul National University (Ph.D)
* Mar. 2013 ~ Feb. 2019: University of Seoul (B.S.)
-->

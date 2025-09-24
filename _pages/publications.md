---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% assign pubs = site.publications | sort: "date" %}

## Journal
* * *
{% for p in pubs reversed %}
  {% if p.type == "Journal" or p.pubtype == "Journal" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Conference
* * *
{% for p in pubs reversed %}
  {% if p.type == "Conference" or p.pubtype == "Conference" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Patents
* * *
{% for p in pubs reversed %}
  {% if p.type == "Patent" or p.pubtype == "Patent" or p.type contains "Patent" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% assign pubs = site.publications | sort: "date" %}

## Conference
* * *
{% for p in pubs reversed %}
  {% assign cat = p.category  | downcase %}
  {% assign typ = p.type      | downcase %}
  {% assign ptype = p.pubtype | downcase %}
  {% assign ven = p.venue     | downcase %}
  {% if cat == "conference" or typ == "conference" or ptype == "conference" or ven contains "conference" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Journal
* * *
{% for p in pubs reversed %}
  {% assign cat = p.category  | downcase %}
  {% assign typ = p.type      | downcase %}
  {% assign ptype = p.pubtype | downcase %}
  {% assign ven = p.venue     | downcase %}
  {% if cat == "journal" or typ == "journal" or ptype == "journal" or ven contains "journal" or ven contains "transactions" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## arXiv
* * *
{% for p in pubs reversed %}
  {% assign cat = p.category  | downcase %}
  {% assign typ = p.type      | downcase %}
  {% assign ptype = p.pubtype | downcase %}
  {% assign ven = p.venue     | downcase %}
  {% if cat == "arxiv" or typ == "arxiv" or ptype == "arxiv" or ven contains "arxiv" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Patents
* * *
{% for p in pubs reversed %}
  {% assign cat = p.category  | downcase %}
  {% assign typ = p.type      | downcase %}
  {% assign ptype = p.pubtype | downcase %}
  {% assign ven = p.venue     | downcase %}
  {% if cat contains "patent" or typ contains "patent" or ptype contains "patent" or ven contains "patent" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

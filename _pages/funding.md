---
layout: archive
title: "연구비 (Funding)"
permalink: /funding/
author_profile: true
---

{% include base_path %}

<div style="width: 50px; border-bottom: 3px solid #b5894b; margin-bottom: 1.5em;"></div>

<div class="funding-list">
{% for item in site.data.funding %}
<div class="funding-item" style="
  border-left: 4px solid {% if item.status == 'ongoing' %}#2a5db0{% else %}#aaa{% endif %};
  background: {% if item.status == 'ongoing' %}#f5f8ff{% else %}#fafafa{% endif %};
  border-radius: 0 6px 6px 0;
  padding: 1em 1.2em;
  margin-bottom: 1.1em;
  box-shadow: 0 1px 3px rgba(0,0,0,0.06);
">
  <div style="display: flex; align-items: center; gap: 0.6em; margin-bottom: 0.3em; flex-wrap: wrap;">
    <span style="
      font-size: 0.72em;
      font-weight: 600;
      padding: 2px 8px;
      border-radius: 20px;
      color: #fff;
      background: {% if item.status == 'ongoing' %}#2a5db0{% else %}#888{% endif %};
      white-space: nowrap;
    ">{% if item.status == 'ongoing' %}진행중{% else %}완료{% endif %}</span>
    <span style="font-size: 0.8em; color: #555;">{{ item.period }}</span>
  </div>

  <p style="margin: 0 0 0.4em; font-size: 1em; font-weight: 600; color: #222; line-height: 1.4;">
    {{ item.title }}
  </p>

  <div style="font-size: 0.85em; color: #444; display: flex; gap: 1.5em; flex-wrap: wrap;">
    <span><i class="fa fa-building" aria-hidden="true" style="margin-right:4px; color:#888;"></i>{{ item.agency }}</span>
    {% if item.program %}
    <span><i class="fa fa-folder-open" aria-hidden="true" style="margin-right:4px; color:#888;"></i>{{ item.program }}</span>
    {% endif %}
    <span><i class="fa fa-user" aria-hidden="true" style="margin-right:4px; color:#888;"></i>{{ item.role }}</span>
    {% if item.amount %}
    <span><i class="fa fa-won-sign" aria-hidden="true" style="margin-right:4px; color:#888;"></i>{{ item.amount }}</span>
    {% endif %}
  </div>
</div>
{% endfor %}
</div>

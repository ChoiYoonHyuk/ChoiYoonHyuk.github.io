---
layout: archive
title: "강의 (Lectures)"
permalink: /lectures/
author_profile: true
---


{% include base_path %}


<!-- > 지금까지 진행한 강의 목록입니다. 각 항목은 `_teaching/` 폴더의 마크다운 파일로부터 자동으로 생성됩니다. -->


{% for post in site.teaching reversed %}
{% include archive-single.html %}
{% endfor %}

---
title: People
permalink: /people/
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "pi|postdoc" | split: "|" %}
<!--{% assign role_array = "pi|postdoc|gradstudent|researchstaff|visiting|others|alumni" | split: "|" %}-->

<div class="pos_header">
{% if role == 'postdoc' %}
<h3>Technical Fellows</h3>
 {% elsif role == 'pi' %}
<h3>Principal Investigators</h3>
 {% endif %}
</div>

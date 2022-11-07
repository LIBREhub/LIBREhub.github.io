---
title: Resources
permalink: /sources/
---

### **Workshops**

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains "newworkshop" %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">- {{ post.title }}</a> (<small>{{post.date | date: "%m/%d/%y" }}</small>)
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>

<hr>

### **Seminars**

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'seminar' %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">- {{ post.title }}</a> (<small>{{post.date | date: "%m/%d/%y" }}</small>)
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>

<hr>

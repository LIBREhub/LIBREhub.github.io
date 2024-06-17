---
title: Resources
permalink: /resources_toggle/
---
# **Resources**
<br>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script>
  $(document).ready(function() {
    $('.toggle-text').click(function() {
      $(this).next('.content').slideToggle();
    });
  });
</script>

### **Workshops**

<p class="toggle-text">Click to toggle Workshops</p>

<div class="content list" style="display: none;">
  {% for post in site.posts %}
    {% if post.categories contains 'workshop' %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">- {{ post.title }}</a> (<small>{{ post.date | date: "%m/%d/%y" }}</small>)
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>

<hr>

### **Seminars**

<p class="toggle-text">Click to toggle Seminars</p>

<div class="content list" style="display: none;">
  {% for post in site.posts %}
    {% if post.categories contains 'seminar' %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">- {{ post.title }}</a> (<small>{{ post.date | date: "%m/%d/%y" }}</small>)
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>

<hr>

### **Other resources**

[GitBuilding for Beginners](https://librehub.github.io/gitbuilding-for-beginners/) - User guide to implement and deploy a GitBuilding website.

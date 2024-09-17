---
title: Resources
permalink: /sources/
---

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script>
  $(document).ready(function() {
    $('.toggle-text').click(function() {
      var content = $(this).next('.content');
      content.slideToggle();
      if (content.is(':visible')) {$(this).text('Show more');}
      else {$(this).text('Show less');}
    });
  });
</script>

<style>
  .toggle-text {
    cursor: pointer;
    color: #007BFF; /* Default color */
    transition: color 0.3s ease; /* Smooth transition for color change */
  }

  .toggle-text:hover {
    color: #FF5733; /* Color when hovered */
  }
</style>

# **Resources**

The Resources section is a comprehensive and curated collection of publications, source files, tools, and educational materials designed to support research and development of open-source bioimaging technologies. Explore the wide array of resources to accelerate your projects and contribute to the growing open-source community.

### **Publications**

<p class="toggle-text">Show more</p>

<div class="content list" style="display: none;">
  
  <h4>2023</h4>
  <p>
    Open hardware: From DIY trend to global transformation in access to laboratory equipment. Wenzel T (2023). PLOS Biology 21(1): e3001931. (<a href="https://doi.org/10.1371/journal.pbio.3001931">Article</a>)
  </p>

  <h4>2022</h4>
  <p>
    Open Hardware in Science: The Benefits of Open Electronics. Oellermann, M., Price-Whelan, A. M., Diego, O., Seabra, R., Wenzel, T., Haley Pace Wilson, & Tanner, R. L. (2022). Integrative and Comparative Biology, Volume 62, Issue 4, October 2022, Pages 1061–1075. (<a href="https://doi.org/10.1093/icb/icac043">Article</a>)
  </p>

  <h4>2020</h4>
  <p>
    Standardisation of Practices in Open Source Hardware Bonvoisin, J., Molloy, J., Häuer, M., & Wenzel, T. (2020). Journal of Open Hardware, 4(1). (<a href="https://doi.org/10.5334/joh.22">Article</a>)
  </p>
</div>

<hr>

### **Tutorials**

<p class="toggle-text">Show more</p>

<div class="content list" style="display: none;">
  <div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 20px;">
  
  <!-- Row 1, Column 1 -->
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/nc4b_7pL66U" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <!-- Row 1, Column 2 -->  
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/0zF3DSOCBSA" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <!-- Row 2, Column 1 -->
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/22zVn0-YkIY" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <!-- Row 2, Column 2 -->
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/Hgo2NIhxlEY" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <!-- Row 3, Column 1 -->
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/fFFRetXSQK0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  </div>
</div>

<hr>

### **Workshops**

<p class="toggle-text">Show more</p>

<div class="content list" style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px;">
  {% for post in site.posts %}
    {% if post.categories contains 'workshop' %}
    <div class="list-item" style="text-align: center;">
      <a href="{{ site.baseurl }}{{ post.url }}">
        <!-- Assuming each post has an image thumbnail, you can reference the thumbnail like this -->
        <img src="/{% if post.header-img %}{{ post.header-img }}{% else %}{{ site.header-img }}{% endif %}" alt="{{ post.title }}" style="width: 100%; height: auto; max-width: 250px;">
      </a>
      <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a><br>
        <small>{{ post.date | date: "%m/%d/%y" }}</small>
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

### **Other resources**

[GitBuilding for Beginners](https://librehub.github.io/gitbuilding-for-beginners/) - User guide to implement and deploy a GitBuilding website.

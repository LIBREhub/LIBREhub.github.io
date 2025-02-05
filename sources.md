---
layout: page
title: Resources
permalink: /sources/
---

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script>
  $(document).ready(function() {
    $('.toggle-text').click(function() {
      var content = $(this).next('.content');
      content.slideToggle();

      if ($(this).text() === 'Show more') {
        $(this).text('Show less');
      } else {
        $(this).text('Show more');
      }
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
Explore recent publications that showcase the principales and impact of open-source hardware in science.
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

### **3D Printing**
Discover our tools, accessories, and instrumentation for bioimaging that can be digitally manufactured.
<p class="toggle-text">Show more</p>

<div class="content list" style="display: none;">

  <div class="content list" style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px;">
    <!-- Printables Designs -->
    <div class="list-item" style="text-align: center;">
      <a href="https://www.printables.com/de/@WenzelLab" target="_blank">
        <img src="/images/printables-thumbnail.png" alt="Printables Designs" style="width: 100%; height: auto; max-width: 250px;">
      </a>
      <p class="list-post-title">
        <a href="https://www.printables.com/de/@WenzelLab" target="_blank">Designs on Printables</a>
      </p>
    </div>
    <!-- Thingiverse Designs -->
    <div class="list-item" style="text-align: center;">
      <a href="https://www.thingiverse.com/libre-hub/designs" target="_blank">
        <img src="/images/thingiverse-thumbnail.png" alt="Thingiverse Designs" style="width: 100%; height: auto; max-width: 250px;">
      </a>
      <p class="list-post-title">
        <a href="https://www.thingiverse.com/libre-hub/designs" target="_blank">Designs on Thingiverse</a>
      </p>
    </div>
  </div>

</div>

<hr>

### **Tutorials**
Learn from a variety of tutorials how to design, implement, and mantain your scientific instrumentation.
<p class="toggle-text">Show more</p>

<div class="content list" style="display: none;">
  <div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 20px;">

  <!-- Row 1, Column 1 -->
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/9ROkLSZw4yw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <!-- Row 1, Column 2 -->  
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/y5xszBXhCEc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <!-- Row 2, Column 1 -->
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/jGoFX0BDh_I" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <!-- Row 2, Column 2 -->  
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/nc4b_7pL66U" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <!-- Row 3, Column 1 -->  
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/0zF3DSOCBSA" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <!-- Row 3, Column 2 -->
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/22zVn0-YkIY" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <!-- Row 4, Column 1 -->
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/Hgo2NIhxlEY" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <!-- Row 4, Column 2 -->
  <iframe width="100%" height="200" src="https://www.youtube.com/embed/fFFRetXSQK0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  </div>
</div>

<hr>

### **Workshops**
Engage with hands-on workshops focused on scientific instrumentation and analysis techniques.
<p class="toggle-text">Show more</p>

<div class="content list" style="display: none;">
  <div class="content list" style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px;">
    {% for post in site.posts %}
      {% if post.categories contains 'workshop' %}
      <div class="list-item" style="text-align: center;">
        <a href="{{ post.docu }}" target="_blank">
          <!-- Assuming each post has an image thumbnail -->
          <img src="/{% if post.header-img %}{{ post.header-img }}{% else %}{{ site.header-img }}{% endif %}" alt="{{ post.title }}" alt="{{ post.title }}" style="width: 100%; height: auto; max-width: 250px;">
        </a>
        <p class="list-post-title">
          <a href="{{ post.docu }}" target="_blank">{{ post.title }}</a><br>
          <small>{{ post.date | date: "%m/%d/%y" }}</small>
        </p>
      </div>
      {% endif %}
    {% endfor %}
  </div>
</div>

<hr>

### **Seminars**
Discover seminars featuring state-of-the-art technologies and key discussions on software and hardware development.
<p class="toggle-text">Show more</p>

<div class="content list" style="display: none;">
  <div class="content list" style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px;">
    {% for post in site.posts %}
      {% if post.categories contains 'seminar' %}
      <div class="list-item" style="text-align: center;">
        <a href="{{ post.video }}" target="_blank">
          <!-- Assuming each post has an image thumbnail -->
          <img src="/{% if post.header-img %}{{ post.header-img }}{% else %}{{ site.header-img }}{% endif %}" alt="{{ post.title }}" style="width: 100%; height: auto; max-width: 250px;">
        </a>
        <p class="list-post-title">
          <a href="{{ post.video }}" target="_blank">{{ post.title }}</a><br>
          <small>{{ post.date | date: "%m/%d/%y" }}</small>
        </p>
      </div>
      {% endif %}
    {% endfor %}
  </div>
</div>

<hr>

### **BioImaging Communities**
Connect with bioimaging communities from across the globe that share resources and expertise.
<p class="toggle-text">Show more</p>

<div class="content list" style="display: none;">
  
  <p>
    Global BioImaging Network (<a href="https://globalbioimaging.org/">Website</a>)
  </p>

  <p>
   BioImaging North America (<a href="https://www.bioimagingnorthamerica.org/">Website</a>)
  </p>

  <p>
   Latin America BioImaging (<a href="https://labi.lat/">Website</a>)
  </p>

  <p>
   African BioImaging Consortium (<a href="https://www.africanbioimaging.org/">Website</a>)
  </p>

  <p>
   Focal Plane Network (<a href="https://focalplane.biologists.com/">Website</a>)
  </p>

  <p>
   Scientific Community Image Forum (<a href="https://forum.image.sc/">Website</a>)
  </p>

</div>


<!--  
### **Other resources**
[GitBuilding for Beginners](https://librehub.github.io/gitbuilding-for-beginners/) - User guide to implement and deploy a GitBuilding website.
-->
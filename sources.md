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
      
      // Toggle the text between "Show more" and "Show less"
      if (content.is(':visible')) {
        $(this).text('Show more');
      } else {
        $(this).text('Show less');
      }
    });
  });
</script>

# **Resources**

The Resources section is a comprehensive and curated collection of publications, source files, tools, and educational materials designed to support research and development of open-source bioimaging technologies. Explore the wide array of resources to accelerate your projects and contribute to the growing open-source community.

### **Publications**
<p class="toggle-text" style="cursor: pointer;">Show more</p>

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

### **Workshops**

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'workshop' %}
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

### **Other resources**

[GitBuilding for Beginners](https://librehub.github.io/gitbuilding-for-beginners/) - User guide to implement and deploy a GitBuilding website.

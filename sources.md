---
title: Resources
permalink: /sources/
---

# **Resources**
<br>

The Resources section is a comprehensive and curated collection of publications, source files, tools, and educational materials designed to support research and development of open-source bioimaging technologies. Explore the wide array of resources to accelerate your projects and contribute to the growing open-source community.

<details>
  <summary><strong>Publications</strong></summary>

  ## **2023**
  _Open hardware: From DIY trend to global transformation in access to laboratory equipment_<br>
  Wenzel T (2023). PLOS Biology 21(1): e3001931. ([Article](https://doi.org/10.1371/journal.pbio.3001931))

  ## **2022**
  _Open Hardware in Science: The Benefits of Open Electronics_<br>
  Oellermann, M., Price-Whelan, A. M., Diego, O., Seabra, R., Wenzel, T., Haley Pace Wilson, & Tanner, R. L. (2022). Integrative and Comparative Biology, Volume 62, Issue 4, October 2022, Pages 1061–1075. ([Article](https://doi.org/10.1093/icb/icac043))

  ## **2020**
  _Standardisation of Practices in Open Source Hardware_<br>
  Bonvoisin, J., Molloy, J., Häuer, M., & Wenzel, T. (2020). Journal of Open Hardware, 4(1). ([Article](https://doi.org/10.5334/joh.22))

</details>

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

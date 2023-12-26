---
title: Workshops
permalink: /workshops/
---

# **Workshops**
<br>
<!--
## Future Workshops
<br>
<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'newworkshop' %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ post.url | prepend: site.baseurl }}">
            <div class="row">
                <div class="col-sm-4">
                <img src="/{% if post.header-img %}{{ post.header-img }}{% else %}{{ site.header-img }}{% endif %}">
                </div>
                <div class="col-sm-8">
                    <h3 class="post-title">
                      {{ post.title }}
                    </h3>
                    <p class="list-post-title" >
                      {{ post.content | strip_html | truncatewords:30 }}
                    </p>
                    <p class="list-detail" style="font-size: 1.2em;">
                      <a class="documentation" href="{{ post.docu }}"><i class="fa fa-book"></i> Documentation</a>
                    </p>
                    <p class="list-detail" style="font-size: 0.87em;">
                      Posted on {{ post.date | date: "%B %-d, %Y" }}
                    </p>
                </div>  
            </div>
            <hr/>
        </a>
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>
<br>
-->
## Past Workshops
<br>
<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'workshop' %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ post.url | prepend: site.baseurl }}">
            <div class="row">
                <div class="col-sm-4">
                    <img src="/{% if post.header-img %}{{ post.header-img }}{% else %}{{ site.header-img }}{% endif %}">
                </div>
                <div class="col-sm-8">
                    <h3 class="post-title">
                      {{ post.title }}
                    </h3>
                    <p class="list-post-title" >
                      {{ post.content | strip_html | truncatewords:30 }}
                    </p>
                    <p class="list-detail" style="font-size: 1.2em;">
                      <a class="documentation" href="{{ post.docu }}"><i class="fa fa-book"></i> Documentation</a>
                    </p>
                    <p class="list-detail" style="font-size: 0.87em;">
                      Posted on {{ post.date | date: "%B %-d, %Y" }}
                    </p>
                </div>  
            </div>
            <hr/>
        </a>
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>

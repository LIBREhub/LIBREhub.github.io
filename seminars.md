---
title: seminars
permalink: /seminars/
---
# **Seminars Series**
<br>

## Future Seminars
<br>
<div class="content list">
  {% for post in site.posts %}
     {% if post.categories contains 'newseminar' %}
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

## Past Seminars
<br>
<div class="content list">
  {% for post in site.posts %}
     {% if post.categories contains 'seminar' %}
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
                            <h4 class="list-post-title">
                                {{ post.speaker }}
                            </h4>
                            <p class="list-detail" >
                              <a class="video" href="{{ post.video }}"><i class="fa fa-youtube"></i> Watch now</a>
                            </p>
                            <p class="list-post-title" >
                              {{ post.content | strip_html | truncatewords:30 }}
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

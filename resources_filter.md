---
title: Resources
permalink: /resources_filter/
---
# **Seminars Series**
<br>

<div class="btn-group">
  <button class="btn btn-default" onclick="filterSeminars('all')">All</button>
  <button class="btn btn-default" onclick="filterSeminars('newseminar')">Future Seminars</button>
  <button class="btn btn-default" onclick="filterSeminars('seminar')">Past Seminars</button>
</div>

<br><br>

<div id="seminars">
  <div class="content list newseminar">
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
                  <h3 class="post-title">{{ post.title }}</h3>
                  <p class="list-post-title">{{ post.content | strip_html | truncatewords:30 }}</p>
                  <p class="list-detail" style="font-size: 0.87em;">Posted on {{ post.date | date: "%B %-d, %Y" }}</p>
                </div>                    
              </div>
              <hr/>
            </a>
          </p>
        </div>
      {% endif %}
    {% endfor %}
  </div>
  <div class="content list seminar">
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
                  <h3 class="post-title">{{ post.title }}</h3>
                  <p class="list-post-title"><strong>Speaker:</strong> {{ post.speaker }}</p>
                  <p class="list-post-title">{{ post.content | strip_html | truncatewords:30 }}</p>
                  <p class="list-detail" style="font-size: 1.2em;">
                    <a class="video" href="{{ post.video }}"><i class="fa fa-youtube"></i> Watch now</a>
                  </p>
                  <p class="list-detail" style="font-size: 0.87em;">Posted on {{ post.date | date: "%B %-d, %Y" }}</p>
                </div>                    
              </div>
              <hr/>
            </a>
          </p>
        </div>
      {% endif %}
    {% endfor %}
  </div>
</div>

<script>
  function filterSeminars(category) {
    var seminars = document.getElementById("seminars").children;
    for (var i = 0; i < seminars.length; i++) {
      if (category === 'all') {
        seminars[i].style.display = 'block';
      } else {
        if (seminars[i].classList.contains(category)) {
          seminars[i].style.display = 'block';
        } else {
          seminars[i].style.display = 'none';
        }
      }
    }
  }
</script>

<style>
  .btn-group {
    display: flex;
    justify-content: center;
    margin-bottom: 20px;
  }
  .btn {
    background-color: #f1f1f1;
    border: 1px solid #ccc;
    padding: 10px 20px;
    cursor: pointer;
  }
  .btn:hover {
    background-color: #ddd;
  }
  .btn-default {
    color: #333;
  }
  .list-item {
    margin-bottom: 20px;
  }
</style>

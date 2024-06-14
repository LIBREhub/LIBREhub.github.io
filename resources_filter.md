---
title: Resources
permalink: /resources_filter/
---
# **Resources**
<br>

<div class="btn-group">
  <button class="btn btn-default" onclick="filterPost('all')">All</button>
  <button class="btn btn-default" onclick="filterPost('seminar')">Seminars</button>
  <button class="btn btn-default" onclick="filterPost('workshop')">Workshops</button>
</div>

<br><br>

<div id="posts" class="grid-container">
  <div class="grid-item seminar">
    {% for post in site.posts %}
      {% if post.categories contains 'seminar' %}
        <div class="list-item">
          <a href="{{ post.url | prepend: site.baseurl }}">
            <img src="/{% if post.header-img %}{{ post.header-img }}{% else %}{{ site.header-img }}{% endif %}" class="post-image">
            <div class="post-content">
              <h3 class="post-title">{{ post.title }}</h3>
              <p class="list-post-title"><strong>Speaker:</strong> {{ post.speaker }}</p>
              <p class="list-post-title">{{ post.content | strip_html | truncatewords:30 }}</p>
              <p class="list-detail" style="font-size: 1.2em;">
                <a class="video" href="{{ post.video }}"><i class="fa fa-youtube"></i> Watch now</a>
              </p>
              <p class="list-detail" style="font-size: 0.87em;">Posted on {{ post.date | date: "%B %-d, %Y" }}</p>
            </div>
          </a>
        </div>
      {% endif %}
    {% endfor %}
  </div>
  <div class="grid-item workshop">
    {% for post in site.posts %}
      {% if post.categories contains 'workshop' %}
        <div class="list-item">
          <a href="{{ post.url | prepend: site.baseurl }}">
            <img src="/{% if post.header-img %}{{ post.header-img }}{% else %}{{ site.header-img }}{% endif %}" class="post-image">
            <div class="post-content">
              <h3 class="post-title">{{ post.title }}</h3>
               <p class="list-post-title">{{ post.content | strip_html | truncatewords:30 }}</p>
                <p class="list-detail" style="font-size: 1.2em;">
                  <a class="documentation" href="{{ post.docu }}"><i class="fa fa-book"></i> Documentation</a>
                </p>
              <p class="list-detail" style="font-size: 0.87em;">Posted on {{ post.date | date: "%B %-d, %Y" }}</p>
            </div>
          </a>
        </div>
      {% endif %}
    {% endfor %}
  </div>
</div>

<script>
  function filterPost(category) {
    var posts = document.getElementById("posts").children;
    for (var i = 0; i < posts.length; i++) {
      var post = posts[i];
      if (category === 'all') {
        post.style.display = 'block';
      } else {
        if (post.classList.contains(category)) {
          post.style.display = 'block';
        } else {
          post.style.display = 'none';
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
    margin: 0 5px;
  }
  .btn:hover {
    background-color: #ddd;
  }
  .btn-default {
    color: #333;
  }
  .grid-container {
    display: grid;
    /*grid-template-columns: auto auto auto auto;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));*/
    /* row-gap: 30px;  /* Increased row gap for more space between rows */
    /* column-gap: 20px;  /* Default column gap 
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    column-gap: 10px;
    row-gap: 15px;
    */
    grid-gap: 10px 15px;
    grid-template-columns: repeat(3, 1fr 2fr);
    grid-template-rows: repeat(2, 100px auto 20%);
  }
  .grid-item {
    border: 1px solid #ccc;
    border-radius: 8px;
    overflow: hidden;
    background-color: #fff;
  }
  .list-item {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .post-image {
    width: 100%;
    height: 300px; /* Reduced height for smaller images */
    object-fit: cover;
  }
  .post-content {
    padding: 15px;
  }
  .post-title {
    font-size: 1.5em;
    margin-bottom: 10px;
  }
  .list-post-title, .list-detail {
    font-size: 1em;
    margin-bottom: 10px;
  }
  .video {
    color: #d9534f;
    text-decoration: none;
  }
  .video:hover {
    text-decoration: underline;
  }
  .documentation {
    color: #337ab7;
    text-decoration: none;
  }
  .documentation:hover {
    text-decoration: underline;
  }
</style>
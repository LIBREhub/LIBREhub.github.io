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

<div id="seminars" class="grid-container">
  <div class="grid-item newseminar">
    {% for post in site.posts %}
      {% if post.categories contains 'newseminar' %}
        <div class="list-item">
          <a href="{{ post.url | prepend: site.baseurl }}">
            <img src="/{% if post.header-img %}{{ post.header-img }}{% else %}{{ site.header-img }}{% endif %}" class="post-image">
            <div class="post-content">
              <h3 class="post-title">{{ post.title }}</h3>
              <p class="list-post-title">{{ post.content | strip_html | truncatewords:30 }}</p>
              <p class="list-detail" style="font-size: 0.87em;">Posted on {{ post.date | date: "%B %-d, %Y" }}</p>
            </div>
          </a>
        </div>
      {% endif %}
    {% endfor %}
  </div>
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
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    row-gap: 30px;  /* Increased row gap for more space between rows */
    column-gap: 20px;  /* Default column gap */
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
    height: 200px; /* Reduced height for smaller images */
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
</style>
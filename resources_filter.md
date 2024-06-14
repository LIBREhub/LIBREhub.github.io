---
title: Resources
permalink: /resources_filter/
---
---
title: Seminars
permalink: /seminars/
---
# **Seminars Series**
<br>

<!-- Filter buttons -->
<div class="filter-buttons">
  <button id="future-seminars-btn" onclick="showFutureSeminars()">Future Seminars</button>
  <button id="past-seminars-btn" onclick="showPastSeminars()">Past Seminars</button>
</div>
<br>

<!-- Future Seminars Section -->
<div id="future-seminars" class="content list">
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
                            <p class="list-post-title">
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

<!-- Past Seminars Section -->
<div id="past-seminars" class="content list" style="display: none;">
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
                            <p class="list-post-title">
                              <strong>Speaker:</strong>  {{ post.speaker }}
                            </p>
                            <p class="list-post-title">
                              {{ post.content | strip_html | truncatewords:30 }}
                            </p>
                            <p class="list-detail" style="font-size: 1.2em;">
                              <a class="video" href="{{ post.video }}"><i class="fa fa-youtube"></i> Watch now</a>
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

<script>
function showFutureSeminars() {
  document.getElementById('future-seminars').style.display = 'block';
  document.getElementById('past-seminars').style.display = 'none';
}

function showPastSeminars() {
  document.getElementById('future-seminars').style.display = 'none';
  document.getElementById('past-seminars').style.display = 'block';
}
</script>
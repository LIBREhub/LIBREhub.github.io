---
title: People
permalink: /people/
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "pi|researchstaff|fellow|gradstudent|communication|alumni" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}

<div class="pos_header">
{% if role == 'fellow' %}
<h3>Technology Fellows</h3>
 {% elsif role == 'pi' %}
<h3>Principal Investigators</h3>
 {% elsif role == 'gradstudent' %}
<h3>Graduate Students</h3>
 {% elsif role == 'researchstaff' %}
<h3>Project Management</h3>
 {% elsif role == 'communication' %}
<h3>Communications</h3>
 {% elsif role == 'alumni' %}
<h3>Past Members</h3>
{% endif %}
</div>

{% if role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.avatar %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
          {% else %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
          {% endif %}
          <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
        </p>
      </div>    
    {% endif %}
  {% endfor %}
</div>
<hr>

{% else %}

<br>

| Who are they | When were they here |
| :------------- |:-------------|
| [Claudia Tapia](https://librehub.github.io/people/claudia_tapia/index.html) | Project Manager (2022 - 2023) | 
| [Tomas Astudillo](https://librehub.github.io/people/tomas_astudillo/index.html) | Technology Fellow (2023) |

{% endif %}
{% endfor %}

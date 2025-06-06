---
title: People
permalink: /people/
---

<style>
    .profile-thumbnail {
      opacity: 1; /* Set the initial opacity to fully visible */
      transition: opacity 0.3s ease; /* Add a smooth transition effect */
    }

    .profile-thumbnail:hover {
      opacity: 0.5; /* Set the opacity when hovering */
    }
</style>

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

<br>

<figure><center>
  <img width="500" src="/images/people/LIBREHub_Team_2025.jpg">
</center></figure>

<br>

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
          <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a><br>
          <a class="email" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.email }}</a>
        </p>
      </div>    
    {% endif %}
  {% endfor %}
</div>
<hr>

{% else %}

| Who are they | When were they here |
| :------------- |:-------------|
| [Claudia Tapia](https://librehub.github.io/people/claudia_tapia/index.html) | Project Manager (2022 - 2023) | 
| [Tomas Astudillo](https://librehub.github.io/people/tomas_astudillo/index.html) | Technology Fellow (2023) |
| Martin Pérez | Software Fellow (2023) |
| [Francisco Martínez](https://librehub.github.io/people/francisco_martinez/index.html) | Technology Fellow (2023 - 2024) |
| [Agnes Marian](https://librehub.github.io/people/agnes_marian/index.html) | Communications Manager (2023 - 2024) |
| [Joaquin Acosta](https://librehub.github.io/people/joaquin_acosta/index.html) | Software Fellow (2024) |

{% endif %}
{% endfor %}

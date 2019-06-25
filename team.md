---
layout: page
title: Golem Foundation Team
permalink: /team/
---

<div id="team-core" class="page-content more-bottom">
  <div class="col-lg-12 col-md-12 col-sm-12">
    <h2 id="core-team" class="text-center more-bottom">Core Team</h2>
  </div>
  {% for team in site.data.team %}
      <div class="row team team-core" id="{{team.name | slugify}}">
        <div class="col-lg-2 col-md-2 col-sm-5 col-xs-12 text-center">
          <div class="picture more-top">
            {% if team.picture %}
            <a href="/team/#{{team.name | slugify}}"><img src="/resources/team/{{team.picture}}" title="Picture of {{team.name}}"></a>
            {% else %}
            <i class="fa fa-user"></i>
            {% endif %}
          </div>
        </div>
        <div class="col-lg-6 col-md-6 col-sm-10 col-xs-12">
          {% assign name_array = team.name | split:" " %}

          <h4 data-anchor-id="{{team.name | slugify}}">{{team.name}}</h4>

          <strong class="role half-bottom">{{team.role}}<br></strong>

          <div class="bio">{{team.bio}}</div>

          {% if team.twitter %}
          <a href="https://twitter.com/{{team.twitter}}" class="link add-right" target="blank"><i class="fa fa-twitter fa-fw"></i>Twitter</a>
          {% endif %}
 
          {% if team.email %}
          <a href="mailto:{{team.email}}" class="link add-right"><i class="fa fa-envelope fa-fw black-icon"></i>Email</a>
          {% endif %}

          {% if team.website %}
          <a href="{{team.website}}" class="link add-right" target="blank"><i class="fa fa-globe fa-fw black-icon"></i>Website</a>
          {% endif %}

          {% if team.linkedin %}
          <a href="https://www.linkedin.com/in/{{team.linkedin}}" class="link add-right" target="blank"><i class="fa fa-linkedin fa-fw"></i>LinkedIn</a>
          {% endif %}

          {% if team.github %}
          <a href="https://github.com/{{team.github}}" class="link" target="blank"><i class="fa fa-github fa-fw black-icon"></i>GitHub</a>
          {% endif %}

        </div>

      </div>
  {% endfor %}
</div>


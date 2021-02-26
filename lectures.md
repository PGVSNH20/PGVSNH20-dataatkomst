---
layout: page
title: Schema
permalink: /lectures/
---

# Lektioner

<div class="row ">
{% for week in site.data.schedule.weeks %}                         
      <div class="col-lg-4">
            <div class="card lectures-card">
                  <div class="card-header text-center">
                        <h4>Vecka: {{week.week}}</h4>
                  </div>
                        <div class="card-body" >
                              <div class="row mt-3">
                              {% for day in week.days %}
                                    {% if day.activities %}
                                    <ul class="list-group lectures-list lec-first">
                                    <h6 class="card-subtitle mb-2 text-muted postlower ml-3">{{ day.day }} - {{day.weekday}}</h6>
                                    {% for activity in day.activities %}
                                    {% if activity.activity == "lecture" %}
                                          <li class="list-group-item">
                                                <i class="bi bi-chevron-double-right lec-icon"></i> <a href="{{ activity.slug | prepend: site.baseurl }}">{{ activity.title }}</a>
                                                {% if activity.discussion %}<a href="{{activity.discussion}}"><i class="fa fa-comments" aria-hidden="true"></i></a><br>{% endif %}
                                                <p class="description"> {{ activity.description }}</p>
                                          </li>
                                    {% endif %}
                                    {% endfor %}
                                    </ul>
                                    {% endif %}
                                    {% endfor %}
                              </div>
                        </div>
                        <div class="card-footer text-center">
                        {{week.description}}
                        </div>
                  </div>
      </div>
{% endfor %}
</div>
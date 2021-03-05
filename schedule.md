---
layout: page
title: Schema
permalink: /schedule/
---

<h1>Schema</h1>

<p>Start: {{ site.course-start}}, slut: {{ site.course-end}}</p>
<div class="section-des">
<table class="table table-bordered border-primary">
  <colgroup>
      <col style="width: 5em"> <!-- Week -->
      <col style="width: 20%;"> <!-- Monday -->
      <col style="width: 20%;"> <!-- Tuesday -->
      <col style="width: 20%;"> <!-- Wednesday -->
      <col style="width: 20%;"> <!-- Thursday -->
      <col> <!-- Friday -->
  </colgroup>
  <thead>
    <tr>
      <th>Vecka</th>
      <th>Måndag</th>
      <th>Tisdag</th>
      <th>Onsdag</th>
      <th>Torsdag</th>
      <th>Fredag</th>
    </tr>
  </thead>
  <tbody>
    {% for week in site.data.schedule.weeks %}
      <tr>
        <th>{{week.week}}</th>
        {% for day in week.days %}
        <td {% if day.background-color %}style="background-color:{{day.background-color}}"{% endif %}>
          {% if day.activities %}
            <div><strong>{{ day.activities[0].start-full | date: "%F"}}</strong></div>
            {% for activity in day.activities %}
            <div class="pt-4">
              {{ activity.start-full | date: "%R"}} - {{ activity.end-full | date: "%R"}}
              <div>
              {% if activity.number %}{{ activity.number }}: {% endif %}{% if activity.slug %}<a href="{{ activity.slug | prepend: site.baseurl }}">{{activity.title}}</a>{% else %}{{activity.title}}{% endif %}
              </div>
            </div>
            {%- endfor -%}
          {% endif %}
        </td>   
        {% endfor %}
      </tr>
    {% endfor %}
  </tbody>
</table>
</div>

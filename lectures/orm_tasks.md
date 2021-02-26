---
layout: lecture
title: ORM och tasks
lectureDate: Onsdag den 10:e Mars 2021
permalink: /lectures/ormtask
---

Denna lektion tittar vi på hur man kan mappa data mot objekt.

Vi försätter även med trådning genom att titta på tasks.

## Lektionsplan
Lektion från kl. 8:30 till kl. 16:30

{% for activity in site.data.schedule.weeks[1].days[2].activities %}
* {{ activity.start-full | date: "%R"}} - {{ activity.end-full | date: "%R"}} : {% if activity.discussion %}<i class="fa fa-comments" aria-hidden="true"></i> [{{activity.title}}]({{activity.discussion}}) (delta aktivt i diskussionen){% else %}{{activity.title}} {% endif %}
{% endfor %}

## Lektionsteori
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*

{% for topic in site.data.lecture_orm_och_tasks.topics %}
### {{topic.topic}}

{% for mandatory in topic.literature %}
* [{{mandatory.title}}]({{mandatory.url}})
{% endfor %}

<details markdown="1">
<summary>Frivillig fördjupningslitteratur innom {{topic.topic}} (klicka för att visa)</summary>
{% for optional in topic.optionalLiterature %}
* [{{optional.title}}]({{optional.url}})
{% endfor %}
</details>

{% endfor %}


## Uppgift

blala
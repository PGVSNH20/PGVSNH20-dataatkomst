---
layout: lecture
title: Trådning uppstart
lectureDate: Måndag den 8:e Mars 2021
permalink: /lectures/threading
---

Denna lektion kommer att vara första lektion med fokus på trådning i C# och .NET.

Trådning är ett komplext ämnen, och vi kommer att återvända till detta, målet är att kunna använda trådning när vi bygger C# applikationer som jobbar med databasen eller andra externa resurser. Men första steg ett är att kunna jobba med trådar.

## Lektionsplan
Lektion från kl. 8:30 till kl. 16:30

{% for activity in site.data.schedule.weeks[1].days[0].activities %}
* {{ activity.start-full | date: "%R"}} - {{ activity.end-full | date: "%R"}} : {% if activity.discussion %}<i class="fa fa-comments" aria-hidden="true"></i> [{{activity.title}}]({{activity.discussion}}) (delta aktivt i diskussionen){% else %}{{activity.title}} {% endif %}
{% endfor %}

## Lektionsteori

{% for mandatory in site.data.lecture_traadning_uppstart.notInTopic.literature %}
* [{{mandatory.title}}]({{mandatory.url}})
{% endfor %}

<details markdown="1">
<summary>Frivillig fördjupningslitteratur (klicka för att visa)</summary>
{% for optional in site.data.lecture_traadning_uppstart.notInTopic.optionalLiterature %}
* [{{optional.title}}]({{optional.url}})
{% endfor %}
</details>


{% for topic in site.data.lecture_traadning_uppstart.topics %}
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
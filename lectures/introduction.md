---
layout: lecture
title: Introduktion till kursen och C# refresh
lectureDate: Måndag den 1:a Mars 2021
permalink: /lectures/introduction
---


Denna lektion är en introduktion till kursen, samt dom första steg med projektet. Fastsällning av grupper.

## Lektionsplan
  <div class="card schedule-card">
          <div class="card-body">
            <div class="row">
                <h5 class="pl-3"><i class="bi bi-calendar-week"></i> Lektion från kl. 8:30 till kl. 16:30 </h5>
            </div>    
{% for activity in site.data.schedule.weeks[0].days[0].activities %}
            <div class="row">
              <div class="col-sm-1 ">
                <div class="circle"></div>
              </div>
              <div class="col-sm-2 p-0 schedule-txt">
             {{ activity.start-full | date: "%R"}} - {{ activity.end-full | date: "%R"}} 
              </div>
              <div class="col-sm-9 schedule-txt">
              {% if activity.discussion %}
              <a href="{{activity.discussion}}">{{activity.title}}</a> <i class="fa fa-comments" aria-hidden="true"></i> 
              (delta aktivt i diskussionen){% else %}{{activity.title}} {% endif %}
              </div>
            </div>
{% endfor %}
          </div>
        </div>




## Lektionsteori
*Detta är material (artiklar, videoer, blogs, podcasts etc) som är den teoretiska bas för denna lektion, det antas att du har läst/set/lystnad detta innan lektionen starter.*

  <div class="accordion" id="accordionExample">
{% for topic in site.data.lecture_csharp_refresh.topics %}
            <div class="card">
                <div class="card-header" id="headingOne">
                  <h2 class="mb-0 w-100">
                    <button class="btn btn-link text-left" type="button" data-toggle="" data-target="#ex{{forloop.index0}}" aria-expanded="false" aria-controls="ex{{forloop.index0}}">
                      <h4 id="object-oriented-programming-and-c"><i class="bi bi-chevron-double-right"></i> 
                      {{topic.topic}}
                      </h4>
                    </button>
                  </h2>
                </div>
                <div id="ex{{forloop.index0}}" class="collapse show" aria-labelledby="headingOne" data-parent="#accordionExample">
                  <div class="card-body">
                  <ul>
                  {% for mandatory in topic.literature %}
                  <li class="mb-3">
                       <i class="bi bi-chevron-double-right lec-icon"></i><a href="{{mandatory.url}}"> {{mandatory.title}}</a>
                      {% if mandatory.timeMinutes %} 
                        <span class="badges"><span class="badge badge-{{mandatory.timeBadge}}">{{mandatory.timeDescription}}</span><span class="badge badge-secondary">{{mandatory.timeMinutes}} min</span></span>
                      {% endif %}
                    </li>
                  {% endfor %}
                  </ul>
                  <details>
                  <summary>Frivillig fördjupningslitteratur innom {{topic.topic}} (klicka för att visa)</summary>
                  <ul>
                  {% for optional in topic.optionalLiterature %}
                  <li class="mb-4">
                  <a href="{{optional.url}}">{{optional.title}}</a>
                  <span class="badges"><span class="badge badge-info">Article</span><span class="badge badge-secondary">12min</span></span>
                  </li>
                  {%endfor%}
                  </ul>
                  </details>
                  </div>
                </div>
                </div>
                
                {% endfor %}
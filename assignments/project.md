---
layout: page
title: Ge­men­samt projekt
permalink: /assignments/project
---

![Lokal på distans](/course-producera-leverera/_images/project_title.png)

Projektet görs i samarbete med en testare-klass på Teknikhögskolan i Stockholm

Al information om projektet finns i [Confluence](https://plushogskolan.atlassian.net/wiki/spaces/TO/overview?homepageId=58589566), och det är altid informationen i Confluense som är det som gäller.

* 2020-12-07 - 2020-12-10: P0 - Projekt grund
* 2020-12-11 (Fredag): P1 - Project introdction
* 2020-12-14 (Måndag): P2 - Hjälp
* 2020-12-15 (Tisdag): P3 - Start sprint 1
* 2020-12-23 (Onsdag): P4 - Slut sprint 1, start sprint 2
* 2021-01-07 (Torsdag): P5 - Slut sprint 2
* 2021-01-11 (Måndag): P6 - Start sprint 3
* 2021-01-13 (Onsdag): P7 - Slut sprint 3
* 2021-01-19: [Redovisning av projekt](https://plushogskolan.atlassian.net/wiki/spaces/TO/pages/75829245/Inf+r+redovisning+tisdagen+den+19+januari)

Alla dagar under sprinten är där [daily standup]({{ "/lectures/standup" | prepend: site.baseurl }}).

## Tech lead
Målet med detta möte är att få ett överblik över tekniska funderingar i alla grupper.
* 2020-12-17, 11:00
* 2020-12-21, 11:00
* 2020-12-28, 11:00
* 2020-12-30, 11:00
* 2021-01-05, 11:00
* 2021-01-12, 11:00

## Projekt krav
Se confluence for senaste version: [System krav](https://plushogskolan.atlassian.net/wiki/spaces/TO/pages/64061445/System+krav)
* Ett SRS dokument på engelska (i markdown)
* Krav skrivs som features med BDD på engelska
* Al kod i ett publikt GitHub repo
* GitHub pull requests
* Confulenece
* Jira

## Tekniska krav
Se confluence for senaste version: [System krav](https://plushogskolan.atlassian.net/wiki/spaces/TO/pages/64061445/System+krav)
* .NET 5 eller .NET Core 3.1
    * C#
* En (eller fler) frontend
    * ASP.NET MVC
    * ASP.NET Razor pages
    * Blazor
    * Xamerin
    * Windows - WPF
    * Windows - UWP
    * React / Angular + Typescript
* En backend
    * REST
    * GraphQL
    * gRPC
* En databas
    * MSSQL
    * MySQL / MariaDb
    * Cosmos
    * MongoDB
* GitHub Action CI/CD
* Deployment till moln AWS eller Azure
* Docker
* Automatiska test
    * Unit tests
    * evt. Integration tests

## Projekt grund
Vad tänker ni att bygga? Börja diskutera, detta kan påverka ert tekniska design

Börja att skåpa en grund till programmet. Skåpa alla projekt och se till att få till namngivning och mapp struktur från början.

Förslag 1: Börja med ett simpelt "view" som visar ett "Hello world", som det hämtar från ett Hello World-endpoint i ert API.

Skriv ett par automatiska test av frontend och backend.

Sätta upp Docker och Docker-compose.

Konfigurara upp GitHub actions. Börja med CI.

Få till deployment av denna Hello World.
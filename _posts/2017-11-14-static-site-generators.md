---
layout:   post
title:    "Static site generators"
date:     2017-11-14 19:59:20 +0100
tags:     [Jekyll, static site generator, SSG, 1dv022]
# imageSrc: /assets/images/humans.png
# imageAlt: människa framför en dator
description: >-
  Det du behöver veta om static site generators och om det passar ditt projekt.
---
Det här är första gången som jag använder mig utav en SSG och redan så ser jag andra tillfällen där jag skulle kunna ha användning av en sådan lösning i framtiden. Det går relativt snabbt att lyckas skapa en site utan att behöva upprepa kod i onödan samtidigt som man slipper lägga in text bland en massa html-element eftesom man kan använda sig av [markdown](https://sv.wikipedia.org/wiki/Markdown). 

Den stora nackdelen mot en blogg med en databas är att det blir lite mer jobb att uppdatera bloggen eftersom webbplatsen måste kompileras om och läggas upp igen. Det är dock något man får igen i säkerhet och snabbhet.

## När ska man använda en SSG?
Om man inte behöver visa specifik information för olika användare eller om du inte behöver ha tillgång till en databas så är en SSG en väldigt bra lösning. Dessutom finns det flera tredjepart lösningar för [kommentarer](/2017/11/12/comments.html) och kontaktformulär så om det är det enda behovet du har av databasen så kan någon av de alternativen fungera lika bra. Däremot om användaren ska kunna logga in eller skapa ett konto så bör du välja en annan lösning än SSG.
---
layout:   post
title:    "Vad är syftet med robots.txt?"
date:     2017-11-16 13:49:29 +0100
tags:     robots.txt SEO spiders 1dv022
imageSrc: /assets/images/robots.png
imageAlt: robots.txt
attribution: clipartkid (clipartkid.com) [<a href="https://creativecommons.org/licenses/by-sa/4.0">CC BY-SA 4.0</a>]
description: >-
  Vad är egentligen robots.txt och hur har jag implementerat det på den här siten?
---
Robots.txt är till för att på ett enkelt sätt säga vad robotar på webben får tillgång till. Kortfattat så kan man säga att det snarare är så att man sätter upp stoppskyltar än låsta dörrar. I slutändan så är det upp till roboten att lyssna på begränsningarna eller inte. Därför är det viktigt att forfarande skydda sig mot robotar och inte ha känsliga uppgifter öppet. Det är även smart att snarare "låsa" en mapp med filerna än att skriva ut url:en till specifika filer eftersom robots.txt-filen är publik så istället blir det lättare för användare att hitta de filerna som du vill gömma. Det är viktigt att lägga filen i rotmappen så att robotarna kan hitta den.

## Värt att tänka på angående SEO
En websidan kan fortfarande indexeras av sökmotorer på andra sätt men Google vill ha tillgång till CSS- och javascript-filer för att kunna läsa sidan ordentligt. Om man inte tillåter det finns risken att hamna längre ner bland sökresultaten.

## Hur min robots.txt är konfiguerad
Jag har valt att gömma alla filer för alla robotar förutom för Google, Yahoo och Bing. Som nämns i stycket tidigare kräver Google tillgång till CSS- och javascript-filer. För att inte riskera sämre sökresultat på andra sidor tillåts alla robotar tillgång till min CSS-fil. Projektet har inga javascript-filer därför är inte de nämnda i robots.txt.

### Innehållet i min robots.txt
```
User-agent: *
Disallow: /
Allow: /*.css$

# Allow google, yahoo and Bing.
User-agent: Googlebot
User-agent: Slurp
User-agent: Bingbot
User-agent: MSNbot
Disallow:
``` 
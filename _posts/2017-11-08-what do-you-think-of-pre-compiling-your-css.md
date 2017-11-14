---
layout:   post
title:    "Min syn på för-kompilerad CSS"
date:     2017-11-08 19:03:29 +0100
tags:     SASS SCSS CSS 1dv022
imageSrc: /assets/images/pre-compiling.png
imageAlt: sass vs. css
description: >-
  En sammanfattning om min erfarenthet och åsikt om att jobba med sass istället för ren CSS.
---
Det här är mitt första projekt där jag använder mig av för-kompilerad CSS. Jag har valt att använda mig av Sass/Scss. Den största fördelen vid första anblick är att man kan på ett tydligare sätt strukturera upp CSS:en men fortfarande bara ha en CSS-fil att ladda in. Ju mer man sätter sig in i det så blir det tydligt att det är flera aspekter som gör livet lättare. Trots det så har jag kommit på mig själv att inte använda mig av Sass lösningar fullt ut. Under tiden jag har jobbat med det så har jag inte kommit fram till någon direkt nackdel förutom möjligtvis att det blir ytterligare en tjänst att använda sig i sin framtagning av webbplatsen.

## Personlig favorit än så länge
Under projektets gång så har jag lekt lite med designen och nya färger så det jag fanns mest användbart är utan tvekan möjligheten att kunna defininera variabler. Trots att CSS nu har stöd för variabler så föredrar jag Sass implementation mer. Den känns mer inuativ och lättanvänd samt att det stöds i alla webbläsare.

## Min struktur
Jag har valt att strukturerar upp CSS:en i flera filer baserat på globala inställningar i filer för basinställningarna och text men även gjort specifika filer för bland annat footer, header och post. Sedan importeras alla filerna till min main.scss som blir det som sedan generas till main.css med alla stilinställningarna.

Om jag hade strukturerat om projektet så hade jag kanske snarare valt att dela upp det i komponenter. Typ navigation (inkl. knappar och länkar), layout osv istället för att minska risken av dubblering av kod. Eftersom det här projektet är så litet så har det gått helt okej med det här upplägget och jag har kunnat bryta ut och strukturerat om när det har blivit dubbletter men det börjar märkas att det blir svårare att underhålla.  
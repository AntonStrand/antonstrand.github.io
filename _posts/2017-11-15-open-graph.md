---
layout:   post
title:    "Sharing is caring"
date:     2017-11-14 19:59:20 +0100
tags:     [Open graph, 1dv022]
imageSrc: /assets/images/open-graph.png
imageAlt: Open graphs logotyp
description: >-
  Hur du på ett snyggt sätt delar din hemsida genom att använda dig av Open Graph.
---
Open Graph Protocol är ett sätt för oss utvecklare att definiera vilket innehåll som ska presenteras när vår sida delas på sociala medier. Det enda man behöver göra är att skapa meta-taggar i sidans header och fylla i den informationen man vill ska visas. Meta-taggen ska innehålla två värden, `property` som används till att berätta vilken typ av information det är och `content` innehåller värdet är på typen. T.ex: `<meta property="og:title" content="Titeln på den delade sidan" />`.

## Det finns fyra obligatoriska property-typer
1. `og:title` - Det är titeln på det som delas.
2. `og:type` - Vad är det för något som delas? 
3. `og:image` - URL:en till en bild som ska visas.
4. `og:url` - URL:en till sidan som delas. Den här används även som ID för Open Graph.

Jag har valt att även lägga till `og:description` som är en kort sammanfattning om vad som visas på sidan och `og:image:alt` som är alt-texten för bilden. Mer information om tillgängliga typerna finns [här](http://ogp.me/).


Den här informationen ska helst vara specifik per sida så jag har använt mig av sidornas YAML front matter för att spara den typen av information. Jag även gjort så att om en sida saknar en bild eller sammanfattning så använder jag mig av en defaultbild och webbplatsens generella beskrivning.

## Hur det blir i praktiken
#### YAML front mattern för den här bloggposten

```
---
layout:   post
title:    "Sharing is caring"
date:     2017-11-14 19:59:20 +0100
tags:     [Open graph, 1dv022]
imageSrc: /assets/images/open-graph.png
imageAlt: Open graphs logotyp
description: >-
  Hur du på ett snyggt sätt delar din hemsida genom att använda dig av Open Graph.
---
```

#### Meta-taggarna i sidans head
Jag har valt att skapa min head som en include och använder mig av liquid för att få fram värdena från den aktuella sidan.
```
{% raw %}
<meta property="og:title" content='{{ page.title }}'/>
<meta property="og:type" content="website" />
<meta property="og:url" content='{{ site.url }}{{ page.url }}' />
{% if page.imageSrc %}
  <meta property="og:image" content={{ site.url }}{{ page.imageSrc }} />
  <meta property="og:image:alt" content="{{ page.imageAlt }}" />
{% else %}
  <meta property="og:image" content="{{ site.url }}/assets/images/anton-strand-avatar.png" />
  <meta property="og:image:alt" content="Sidans defaultbild" />
{% endif %}
<meta property="og:description" content="{% if page.description %}{{ page.description }}{% else %}{{ site.description }}{% endif %}" />
{% endraw %}
```
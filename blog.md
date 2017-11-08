---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: blog
title: Blogg
---

![site.post[0].alt]({{ site.posts[0].image}})
# {{ site.posts[0].title }}
{{ site.posts[0].date | date: "%-d %B - %Y"}}

{{ site.posts[0].excerpt }}

[read more]({{ site.posts[0].url }})


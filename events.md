---
layout: page
title: events
lang: en
ref: events
permalink: /events/
---

**Current Time (Geneva):** {{site.time}}

## ongoing

{% for p in site.events %}
  {% if p.layout == page.title and p.starts < site.time and p.ends > site.time %}<p><h4><a href="{{p.url}}">{{p.title}}</a></h4></p>
    {% if post.excerpt %}
        {{ post.excerpt }}
    {% endif %}
  {% endif %}
{% endfor %}



## upcoming events

{% for p in site.events %}
  {% if p.layout == page.title and p.starts > site.time %}<p><h4><a href="{{p.url}}">{{p.title}}</a></h4></p>
      {% if post.excerpt %}
          {{ post.excerpt }}
      {% endif %}
    {% endif %}
{% endfor %}


## past events

{% for p in site.events %}
  {% if p.layout == page.title and p.ends < site.time %}<p><h4><a href="{{p.url}}">{{p.title}}</a></h4></p>
    {% if post.excerpt %}
        {{ post.excerpt }}
    {% endif %}
  {% endif %}
{% endfor %}

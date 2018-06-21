---
layout: default
title: Talks
navigation_weight: 2
---

# {{ page.title }}

## Mini-courses 
{% assign speakers = site.data.mini-course-abstracts | sort: 'lastname' %}
{% for speaker in speakers %}
<div class="mini-course-abstract">
{% capture speakername %}{{ speaker.firstname }} {{ speaker.lastname }} {% endcapture %}
<h3 id="{{ speakername | slugify }}">{{ speakername }}{% if speaker.title %} — {{speaker.title}}{% endif %}</h3>
{% if speaker.abstract %}{{ speaker.abstract }}<br/>
{% for lecture in speaker.lectures %}
1. **{{ lecture.title}}:** {{ lecture.abstract }}
{% endfor %}
{% endif %}
</div>
{% endfor %}

## Research talks
{% assign speakers = site.data.research-talk-abstracts | sort: 'lastname' %}
{% for speaker in speakers %}
<div class="research-talk-abstract">
**{{ speaker.firstname }} {{speaker.lastname}}{% if speaker.title %}: {{speaker.title}}{% endif %}**
{% if speaker.abstract %}<br/>{{ speaker.abstract }}{% endif %}
</div>
{% endfor %}


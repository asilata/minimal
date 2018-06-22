---
layout: default
title: Talks
navigation_weight: 3
---

# {{ page.title }}

## Mini-courses 
{% assign speakers = site.data.mini-course-abstracts | sort: 'lastname' %}
{% for speaker in speakers %}

<div class="abstract">
{% capture speakername %}{{ speaker.firstname }} {{ speaker.lastname }} {% endcapture %}
<h3 id="{{ speakername | slugify }}">{{ speakername }}{% if speaker.title %} — {{speaker.title}}{% else %} — TBA{% endif %}</h3>
{% if speaker.abstract %}{{ speaker.abstract }}{% endif %}
</div>

{% endfor %}

## Research talks
{% assign speakers = site.data.research-talk-abstracts | sort: 'lastname' %}
{% for speaker in speakers %}

<div class="abstract">
{% capture speakername %}{{ speaker.firstname }} {{ speaker.lastname }} {% endcapture %}
<h3 id="{{ speakername | slugify }}">{{ speakername }}{% if speaker.title %} — {{speaker.title}}{% else %} — TBA{% endif %}</h3>
{% if speaker.abstract %}{{ speaker.abstract }}<br/>
{% for lecture in speaker.lectures %}
1. **{{ lecture.title}}:** {{ lecture.abstract }}
{% endfor %}
{% endif %}
</div>
{% endfor %}


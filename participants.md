---
layout: default
navigation_weight: 5
title: Participants
---

## List of participants

{% assign participants = site.data.participants | sort: 'lastname' %}
<ul>
{% for participant in participants %}
<li>{{ participant.firstname }} {{ participant.lastname }}</li>
{% endfor %}
</ul>

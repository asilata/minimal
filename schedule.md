---
layout: default
title: Program
navigation_weight: 2
---

# {{ page.title }}

<table>
<thead><tr><th></th><th>Monday</th><th>Tuesday</th><th>Wednesday</th><th>Thursday</th><th>Friday</th></tr></thead><tbody>
 <tr>
 <td>08:30</td> <td>Registration</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td>
 </tr>
 <tr>
 <td class="time">09:00</td>
 <td rowspan="2" class="talk">Stroppel 1</td>
 <td rowspan="2" class="talk">Stroppel 2</td>
 <td rowspan="2" class="talk">Proudfoot 2</td>
 <td rowspan="2" class="talk">Stroppel 3</td>
 <td rowspan="2" class="talk">Gordon 3</td>
 </tr>
 <tr></tr>
 <tr>
 <td>10:00</td>
 <td rowspan="2" class="break">Coffee</td>
 <td rowspan="2" class="break">Coffee</td>
 <td class="break">Coffee</td>
 <td rowspan="2" class="break">Coffee</td>
 <td rowspan="2" class="break">Coffee</td></tr>
 <tr>
 <td>10:15</td>
 <td rowspan="3">Gordon 1</td>
 </tr>
 <tr>
 <td>10:30</td>
 <td rowspan="3">Kanstrup</td>
 <td rowspan="3">Negut 2</td>
 <td rowspan="3">Negut 3</td>
 <td rowspan="3">Shapiro</td>
 </tr>
 <tr>
 <td>11:00</td>
 </tr>
 <tr>
 <td>11:15</td>
 <td>Coffee</td>
 </tr>
 <tr>
 <td>11:30</td>
 <td rowspan="4">Lunch</td><td rowspan="4">Lunch</td><td rowspan="2">PS 3</td><td rowspan="4">Lunch</td><td rowspan="4">Lunch</td>
 </tr>
 <tr>
 <td>12:00</td>
 </tr>
 <tr>
 <td>12:30</td>
 <td rowspan="2">Lunch</td>
 </tr>
 <tr><td>13:00</td>
 </tr>
 <tr><td>13:30</td>
 <td rowspan="2">Negut 1</td>
 <td rowspan="2">Proudfoot 1</td>
 <td rowspan="7">Free afternoon</td>
 <td rowspan="2">Gordon 2</td>
 <td rowspan="2">Proudfoot 3</td>
 </tr>
 <tr><td>14:00</td></tr>
 <tr><td>14:30</td><td>Coffee</td>
 <td rowspan="2">PS 2</td>
 <td>Coffee</td><td>Coffee</td></tr>
 <tr><td>15:00</td>
 <td rowspan="2">Mirković</td><td rowspan="2">Saunders</td><td rowspan="2">Sutherland</td></tr>
 <tr><td>15:30</td><td rowspan="4">Poster session</td></tr>
 <tr><td>16:00</td><td rowspan="2">PS 1</td>
 <td rowspan="2">PS 4</td>
 <td rowspan="2">PS 5</td></tr>
 <tr><td>16:30</td></tr>
 <tr><td>17:00</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td>18:00</td><td>&nbsp;</td><td>Conference Dinner</td><td>&nbsp;</td><td>&nbsp;</td><td></td></tr>
</tbody></table>

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


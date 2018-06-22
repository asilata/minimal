---
layout: default
navigation_weight: 1
title: Home
---

## About the summer school

The topic of the summer school is geometric representation theory, with an emphasis on quiver varieties, symplectic resolutions, quantization, and cluster algebras. 
A major goal of geometric representation theory is to reveal unifying geometric and categorical perspectives on classical representation-theoretic objects, and to use these perspectives to solve long-standing algebraic problems. Quiver varieties, and more generally symplectic resolutions, precipitate geometric realizations of various non-commutative algebras and lead to a deeper understanding of the representation theory of these algebras. The non-commutative algebras of interest include algebras of differential operators, enveloping algebras, and quantum groups. More recently, cluster algebras have emerged as a major bridge between a vast array of mathematical topics. 

The aim of the summer school is to provide mini-courses on active themes in geometric representation theory, including those mentioned above. In addition, there will be research talks on recent progress in the field, and a poster session featuring work of graduate students.

[The summer school poster (pdf).](assets/poster.pdf)


## Mini-course speakers

{% assign speakers = site.data.mini-course-abstracts | sort: 'lastname' %}

<ul>
{% for speaker in speakers %}
{% capture speakername %}{{ speaker.firstname }} {{ speaker.lastname }} {% endcapture %}
<li>{% if speaker.website %}
<a href="{{ speaker.website }}">{{ speakername }}</a>
{% else %}{{ speakername }}
{% endif %}
{% if speaker.affiliation %}<em>({{ speaker.affiliation }})</em>{% endif %}
{% if speaker.title %} — <a href="schedule.html#{{ speakername | slugify }}">{{ speaker.title }}</a>{% else %} — TBA{% endif %}
</li>
{% endfor %}
</ul>

## Research talk speakers

{% assign speakers = site.data.research-talk-abstracts | sort: 'lastname' %}

<ul>
{% for speaker in speakers %}
<li>{% if speaker.website %}
<a href="{{ speaker.website }}">{{ speaker.firstname }} {{ speaker.lastname }}</a>
{% else %}{{ speaker.firstname }} {{ speaker.lastname  }}
{% endif %}
{% if speaker.affiliation %}<em>({{ speaker.affiliation }})</em>{% endif %}
{% if speaker.title %} — <a href="schedule.html#{{ speakername | slugify }}">{{ speaker.title }}</a>{% else %} — TBA{% endif %}
</li>
{% endfor %}
</ul>

## Registration and deadlines

[Here](registration) is the link to the registration page.
The registration deadline is **31 March 2018**.
The conference dates are **9 July to 13 July 2018**.


## Organizers and contact

The conference is organized by Asilata Bapat, Iordan Ganev, Tamas Hausel, Maitreyee Kulkarni, and Jacob Matherne.
To get in touch with the organizers, please write to **ssgrt2018@gmail.com**.


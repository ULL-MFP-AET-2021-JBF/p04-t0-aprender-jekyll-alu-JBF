---
layout: page
title: Tareas
permalink: /tareas/
---

{%- for tarea in site.tareas %}
  {%- if tarea.visible %}
{{ tarea.name | slice: 0, 10  }}.  <a href="{{ tarea.url }}">Ver {{ tarea.name }}</a>
  <p>{{ tarea.name }} - {{ tarea.date }}</p>
  <p>{{ tarea.content | markdownify }}</p>
  <p> </p>
  {%- endif %}
{%- endfor %}

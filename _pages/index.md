---
layout: page
title: Home
id: home
permalink: /
---

# Hey ✌️

Este é o meu jardim digital, uma maneira calma e ponderada de existir na web. 
Talvez dure muito tempo, talvez não.

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  Dê uma olhada na <span style="font-weight: bold">[[Minha primeira nota]]</span> para começar a explorar.
</p>

<strong>Últimas atualizações</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>

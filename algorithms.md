---
layout: page
title: Algorithms
permalink: /algorithms/
---

This page will display a table of algorithms.

<table>
  {% for row in site.data.algorithms %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>
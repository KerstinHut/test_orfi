---
layout: default
title: Algorithms
permalink: /algorithms/
dataTable: true
---

This page will display a table of algorithms.

<table class="display">
  {% for row in site.data.algorithms %}
    {% if forloop.first %}
    <thead>
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    </thead>
    {% endif %}
    
    <tbody>
    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
    </tbody>
  {% endfor %}
</table>


<script>
$('table.display').DataTable({
    paging: false,
    scrollY: true,
    scrollX: true
})
</script>
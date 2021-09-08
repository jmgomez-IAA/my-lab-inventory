---
layout: page
title: Inventario
permalink: /inventario/
---

Esta pagina incluye en una tabla el material disponible para el equipo PLATO.

Todos los datos estan almacendados en el fichero .csv, lab_inventory.csv y pueden ser editados sin recompilar.

Puedes encontrar los datos que se muestran en:
_data/lab_inventory.csv

<table>
  {% for row in site.data.lab_inventory %}
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


[jekyll-organization]: https://github.com/jekyll

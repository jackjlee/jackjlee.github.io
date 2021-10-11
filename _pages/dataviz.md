---
title: Data Viz
permalink: /dataviz/
layout: splash
header:
  image: /assets/images/splash-image-circuit.png
  caption: "[Image by Michael Schwarzenberger from Pixabay](https://pixabay.com/users/blickpixel-52945/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=453758)"
---

{% for d in site.data.dataviz -%}
  <h2>{{ d.category }}</h2>
  <ul>
  {%- for v in d.viz -%}
      <li>{{ v.date }}: <a href = "{{ v.url }}">{{ v.title }}</a></li>
      <ul>
        <li style="font-size:90%; font-style:italic;">{{ v.note1-code }}</li>
        {%- if v.note2-archive.size > 0 -%}
          <li style="font-size:90%; font-style:italic;">{{ v.note2-archive }}</li>
        {%- endif -%}
        {%- if v.note3-link.size > 0 -%}
          <li style="font-size:90%; font-style:italic;">{{ v.note3-link }}</li>
        {%- endif -%}
        {%- if v.note4-data.size > 0 -%}
          <li style="font-size:90%; font-style:italic;">{{ v.note4-data }}</li>
        {%- endif -%}
      </ul>
  {%- endfor -%}
  </ul>
{%- endfor %}

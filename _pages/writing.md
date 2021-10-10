---
title: Writing
permalink: /writing/
layout: splash
header:
  image: /assets/images/splash-image-keyboard.png
  caption: "[Image by jacqueline macou from Pixabay](https://pixabay.com/users/jackmac34-483877/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1726000)"
---

{% for w in site.data.writing -%}
  <h2>{{ w.outlet }}</h2>
  {%- for c in w.categories -%}
    {%- if c.category-name.size > 0 -%}
      <h3>{{ c.category-name }}</h3>
    {%- endif -%}
    <ul>
    {%- for s in c.stories -%}
      <li>{{ s.date }}: <a href = "{{ s.url }}">{{ s.title }}</a></li>
      {%- if s.note.size > 0 -%}
        <ul>
        {%- for n in s.note -%}
          <li style="font-size:90%; font-style:italic;">{{ n }}</li>
        {%- endfor -%}
        </ul>
      {%- endif -%}
    {%- endfor -%}
    </ul>
  {%- endfor -%}
{%- endfor %}

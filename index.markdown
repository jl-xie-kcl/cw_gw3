---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Chinese mianshi
layout: index
---
<div id = "gallery">
{% for exhibit in site.exhibits %}

  {% assign licence_url = site.data.licences | find: "licence", exhibit.licence %}
 <div class = "grid_cell">
  <a href = "{{ exhibit.url | relative_url }}"><img src="{{ exhibit.image-url }}" width = 256></a>
  <p><a href = "{{ exhibit.url | relative_url }}">{{ exhibit.title }}</a></p>
  <p><a href="{{ licence_url.url }}">{{ exhibit.licence }}</a></p>
</div>
{% endfor %}
</div>

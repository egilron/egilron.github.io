---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
  __31. juli:__ Jeg skulle prøve meg med nye themes, og da ble layouten med topp-og bunntekst borte. Må få fiksa det.
.
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

[Om meg](https://egilron.github.io/about/)
---
layout: page
title: Authors
permalink: /authors/
---

<ul>
  {% for author in site.authors %}
    <li>
      <a href="{{ author.url }}">{{ author.name }}</a>
      <p>{{ author.content | markdownify }}</p>
    </li>
  {% endfor %}
</ul>

<h2> More Info </h2>

* [https://jekyllrb.com/docs/collections/](https://jekyllrb.com/docs/collections/)
* [https://jekyllrb.com/docs/step-by-step/09-collections/](https://jekyllrb.com/docs/step-by-step/09-collections/)

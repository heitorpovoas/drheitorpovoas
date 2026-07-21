---
layout: page
title: Literatura comentada
permalink: /literatura-comentada/
description: >-
  Análise crítica de evidência recente em cirurgia bariátrica, metabólica e
  medicina da obesidade. Leitura honesta dos estudos que importam — o que
  mostram, e o que não mostram.
---

Análise crítica da literatura recente em cirurgia bariátrica, metabólica e medicina da obesidade. Cada texto pega um estudo relevante (ou alguns que conversam entre si), lê o desenho e as limitações com honestidade, e traduz o que muda — ou não — na prática clínica. Sem manchete, sem panfleto.

{% assign lc_posts = site.posts | where_exp: "post", "post.tags contains 'literatura-comentada'" %}
{% if lc_posts.size > 0 %}
{% for post in lc_posts %}
{{ post.date | date: "%d %b %Y" }}

### [{{ post.title }}]({{ post.url | relative_url }})

{{ post.description }}

[Ler artigo completo →]({{ post.url | relative_url }})

{% endfor %}
{% else %}
*Em breve, os primeiros textos desta seção.*
{% endif %}

---
layout: cards
title: Blog
permalink: /blog/
---
<div class="container">
<div class="row">
<div class="col">
<div class="card-columns blog">
{% for post in site.posts %}
<div class="card hover-shadow mb-3">
<a href="{{ post.url }}" title="{{ post.linktitle | escape}}">
<img 
    src="/img{{ post.url }}lqip_{{ post.img }}" 
    data-sizes="auto"
    data-srcset="
        /img{{ post.url }}lqip_{{ post.img }} 25w,
        /img{{ post.url }}low_{{ post.img }} 500w,
        /img{{ post.url }}med_{{ post.img }} 1000w,
        /img{{ post.url }}high_{{ post.img }} 2000w"
    alt="{{ post.caption }}" 
    class="card-img-top lazyload"
>
</a>
<div class="card-block">
<h4 class="card-title"><a href="{{ post.url }}" title="{{ post.linktitle | escape}}">{{ post.linktitle }}</a></h4>
</div>
<footer class="rounded-bottom">
<a href="/blog/author/{{ post.author }}" title="Browse other posts by this author">{{ post.author }}</a>
in <a href="/blog/category/{{ post.categories }}" title="Browse other posts in this category">{{ post.categories }}</a>
on {{ post.date | date_to_string }}
</footer>
</div>
{% endfor %}
</div>
</div>
</div>
</div>

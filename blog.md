---
layout: page
title: Golem Foundation Blog
permalink: /blog/
---

<div class="home">
    {% for post in site.posts %}
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        <span class="post-meta"> {{ post.date | date: "%b %-d, %Y" }}</span>
    {% endfor %}
</div>

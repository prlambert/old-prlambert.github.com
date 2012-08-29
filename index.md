---
layout: default
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}

<div class="header">
          <!-- <h1><a href="{{ site.url }}">{{ site.title }}</a></h1> -->
    <h1 class="topheader">{{ site.title }}</h1>      
	<h2>{{ site.tagline }}</h2>
</div>

{% for post in site.posts %}
<article>

    <header>
      <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
      <p class="date">{{ post.date | date_to_string }}</p>
    </header>

</article>


{% endfor %}

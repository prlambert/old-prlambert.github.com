---
layout: default
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}


<ul class="posts">
  {% for post in site.posts %}
  <article>

    	<header>
    	  <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
    	  <p class="date">{{ post.date | date_to_string }}</p>
    	</header>

    </article>


  {% endfor %}
</ul>


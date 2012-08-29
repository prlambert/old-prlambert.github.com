---
layout: post
title: "Neat Scala null  > option idiom"
description: ""
category: 
tags: []
---
{% include JB/setup %}

Working with Java APIs in Scala? Things potentially being null when you wish they were None? 

I had this problem working with servlets… request.getQueryString returns null if there is no query string in the url (as opposed to an empty string) and without explicating checking for nulls (a good 3-4 lines of clutter), the code throws an unhelpful null pointer exception. Turns out Option(value) does exactly the type of conversion I want: a Some[return type] or None if it’s null. 

so checking for null conditional (4-5 lines) becomes a single line: 

val queryString = Option(request.getQueryString).getOrElse(throw new NotLoggedInException)

nice

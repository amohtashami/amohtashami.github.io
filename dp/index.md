---
layout: default
title: Design Patterns
categories: home
folder: dp
---
<style type="text/css">
<!--
 .tab { margin-left: 40px; }
-->
</style>


<h1>{{ page.title }}</h1>
<ul class="posts">

{% assign chapKeys_chapValues = "Behavioral, Structural, Creational"  | split: ", "%}

{% for key in chapKeys_chapValues  %}
	<h2>{{key}}</h2>
  	{% assign child_cat = page.folder | append: '\' | append: key %}
  	{% for post in site.categories[child_cat] %}
  	<li class="tab">
   		<a  href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a> 
  	</li>
  	{% endfor %}  
  	<br>
{% endfor %}


 

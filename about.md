---
layout: page
permalink: /about/index.html
title: Erkan Güzeler
tags: [Erkan, Güzeler, ekoerk, erkanguzeler]
imagefeature: fourseasons.jpg
chart: true
---
<figure>
  <img src="{{ site.url }}/images/erkanguzeler.jpg" style="border-radius: 50%;" alt="Erkan Güzeler">
  <figcaption>Erkan Güzeler</figcaption>
</figure>

{% assign total_words = 0 %}
{% assign total_readtime = 0 %}
{% assign featuredcount = 0 %}
{% assign statuscount = 0 %}

{% for post in site.posts %}
    {% assign post_words = post.content | strip_html | number_of_words %}
    {% assign readtime = post_words | append: '.0' | divided_by:200 %}
    {% assign total_words = total_words | plus: post_words %}
    {% assign total_readtime = total_readtime | plus: readtime %}
    {% if post.featured %}
    {% assign featuredcount = featuredcount | plus: 1 %}
    {% endif %}
{% endfor %}


My name is **Erkan Güzeler**, and this is my personal blog. It currently has {{ site.posts | size }} posts in {{ site.categories | size }} categories which combinedly have {{ total_words }} words, which will take an average reader ({{ site.wpm }} WPM) approximately <span class="time">{{ total_readtime }}</span> minutes to read. {% if featuredcount != 0 %}There are <a href="{{ site.url }}/featured">{{ featuredcount }} featured posts</a>, you should definitely check those out.{% endif %} The most recent post is {% for post in site.posts limit:1 %}{% if post.description %}<a href="{{ site.url }}{{ post.url }}" title="{{ post.description }}">"{{ post.title }}"</a>{% else %}<a href="{{ site.url }}{{ post.url }}" title="{{ post.description }}" title="Read more about {{ post.title }}">"{{ post.title }}"</a>{% endif %}{% endfor %} which was published on {% for post in site.posts limit:1 %}{% assign modifiedtime = post.modified | date: "%Y%m%d" %}{% assign posttime = post.date | date: "%Y%m%d" %}<time datetime="{{ post.date | date_to_xmlschema }}" class="post-time">{{ post.date | date: "%d %b %Y" }}</time>{% if post.modified %}{% if modifiedtime != posttime %} and last modified on <time datetime="{{ post.modified | date: "%Y-%m-%d" }}" itemprop="dateModified">{{ post.modified | date: "%d %b %Y" }}</time>{% endif %}{% endif %}{% endfor %}. The last commit was on {{ site.time | date: "%A, %d %b %Y" }} at {{ site.time | date: "%I:%M %p" }} [UTC](http://en.wikipedia.org/wiki/Coordinated_Universal_Time "Temps Universel Coordonné").


I was born in Akseki and a big part of my life passed in Alanya so I had a childhood in a hot part of Turkey. I’m a music addict and an Analog Photographer. I always like to play enstruments like I had participated some concerts to play Darbuka. I also enjoy to do different sports like swimming, cycling,running etc. When I have enough time I took film photography and share [instagram](https://instagram.com/erkan.guzeler). Actually you can follow me

My technical expertise and hobbies are generally about technology. Such as Android Program Development, Java Technologies, Design Patterns, Embedded Linux Technologies, Wireless Technologies, C/C++ Programming Language, Image Processing …
Here is my [Linkedin](https://www.linkedin.com/in/erkan-güzeler-95b47252) professional profile.

*Beautiful, practical, meaningful stuff.*

***To Beatiful Days...***
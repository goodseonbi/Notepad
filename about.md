---
layout: page
permalink: /about/index.html
title: Good Seon Bi
tags: [SeonBiTV, GoodSeonBi]
imagefeature: fourseasons.jpg
chart: true
---
<figure>
  <img src="{{ site.url }}/images/GoodSeonBi.jpg" alt="Good Seon Bi">
  <figcaption>Good Seon Bi</figcaption>
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


My name is **Good Seon Bi**, and this is my Publicly blog. 

**Korean**

이 사이트에는 {{ site.posts | size }} 개의 글과 {{ site.categories | size }} 개의 카테고리가 존재하며 {% if featuredcount != 0 %} <a href="{{ site.url }}/featured">{{ featuredcount }} 추천 게시물</a> 이 있습니다. 총 {{ total_words }} 개의 글자로 여러분에게 대략 ({{ site.wpm }} WPM) <span class="time">{{ total_readtime }}</span> 분 동안의 읽을 거리를 제공합니다.  {% endif %} 가장 최근 글은 {% for post in site.posts limit:1 %}{% if post.description %}<a href="{{ site.url }}{{ post.url }}" title="{{ post.description }}">"{{ post.title }}"</a>{% else %}<a href="{{ site.url }}{{ post.url }}" title="{{ post.description }}" title="Read more about {{ post.title }}">"{{ post.title }}"</a>{% endif %}{% endfor %} 이며 작성된 시간은 {% for post in site.posts limit:1 %}{% assign modifiedtime = post.modified | date: "%Y%m%d" %}{% assign posttime = post.date | date: "%Y%m%d" %}<time datetime="{{ post.date | date_to_xmlschema }}" class="post-time">{{ post.date | date: "%d %b %Y" }}</time>{% if post.modified %}{% if modifiedtime != posttime %} and last modified on <time datetime="{{ post.modified | date: "%Y-%m-%d" }}" itemprop="dateModified">{{ post.modified | date: "%d %b %Y" }}</time>{% endif %}{% endif %}{% endfor %} 입니다.

**착한선비** 는 **다음팟** 과 **트위치TV** 에서 방송을 하고 있으며, 차후 **아프리카TV** 나 다양한 인터넷 방송국을 운영할 계획이다. 주로 **게임**을 주제로 **PS4** 와 **PC**로 방송을 한다. 방송 녹화분들은 **유투브**에 업로드 하며 최대한 고화질의 영상을 업로드 하도록 노력 중이다. 나긋나긋하면서 느끼한 목소리로 진행하며 방송을 시작한 날짜는 2016-03-10 이다. 
adsf

*[착한선비]: GoodSeonBi 의 한글이름
*[다음팟]: 다음에서 서비스 하는 개인 인터넷 방송 서비스
*[트위치TV]: 게임 전용 인터넷 개인 방송 서비스
*[아프리카TV]: 대한민국에서 가장 큰 개인 인터넷 방송 서비스
*[adsf]: 안녕asdf

이 사이트를 방문해주신 모든 시청자분들에게 재미난 방송을 제공하도록 노력하겠습니다.

**감사합니다**


**English**

Coming soon....
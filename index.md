---
layout: home
---
<p class="intro"><b>Previously:</b> {{ site.data.news.news[0].yesterday }}</p>
<h2 class="today"><time class="timeago" datetime="{{ site.data.news.news[0].date }}">{{ site.data.news.news[0].date }}</time></h2>
<ul class="today">
{% for today in site.data.news.news[0].todays %}
 <li>{{ today.item }} <span class="small">(Source: <a href="{{ today.url }}">{{ today.source }}</a>)</span></li>
{% endfor %}
  </ul>

<p class="outtro"><b>What's coming next:</b> {{ site.data.news.news[0].tomorrow }}</p>

<h3>Get caught up further with <a href="archive"> the archive</a></h3>



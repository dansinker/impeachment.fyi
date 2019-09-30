---
layout: home
---
<p class="intro"><b>Previously on The Impeachment:</b> {{ site.data.news.news[0].yesterday }}</p>

<p class="today"><b>Today</b></p>
<ul class="today">
{% for today in site.data.news.news[0].todays %}
 <li>{{ today.item }} <span class="small">(Source: <a href="{{ today.url }}">{{ today.source }}</a>)</span></li>
{% endfor %}
  </ul>

<p class="intro"><b>What's coming next:</b> {{ site.data.news.news[0].tomorrow }}</p>

<p class="intro">Check <a href="archive"> the archive</a> for previous updates.</p>

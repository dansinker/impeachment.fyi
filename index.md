---
layout: home
---
<p class="intro"><b>Where we're at:</b> {{ site.data.news.news[0].yesterday }}</p>

<p class="today"><b>Today</b></p>
<ul class="today">
{% for today in site.data.news.news[0].todays %}
 <li>{{ today.item }}</li>
{% endfor %}
  </ul>

<p class="intro"><b>Watch to Watch For:</b> {{ site.data.news.news[0].tomorrow }}</p>

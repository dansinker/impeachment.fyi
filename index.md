---
layout: home
---
<p class="alert"><b>JAN 8 UPDATE: Impeachment.fyi will relaunch on Monday, January 11, if the House starts a new impeachment proceeeding. For a full account of the <i>last</i> impeachment from start to finish, <a href="/archive">visit the archive</a>. Until Monday, this page remains in the state it was in when the 2020 trial ended.</b></p> 
<p class="intro"><b>Previously:</b> {{ site.data.news.news[0].yesterday }}</p>
<h2 class="today"><time class="timeago" datetime="{{ site.data.news.news[0].date }}">{{ site.data.news.news[0].date }}</time></h2>
<ul class="today">
{% for today in site.data.news.news[0].todays %}
 <li>{{ today.item }} <span class="small">{% if today.source != null %}(Source: <a href="{{ today.url }}">{{ today.source }}</a>){% endif %}</span></li>
{% endfor %}
  </ul>

<p class="outtro"><b>What's coming next:</b> {{ site.data.news.news[0].tomorrow }}</p>





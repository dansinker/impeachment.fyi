---
layout: home
---
<!--<p class="alert"><b>Please note: When the impeachment trial ended on February 5, 2020, so did impeachment.fyi. This page is presented as it was last updated. For a full account of the impeachment from start to finish, <a href="/archive">visit the archive</a>.</b></p> -->
<p class="intro"><b>Previously:</b> {{ site.data.newnews.news[0].yesterday }}</p>
<h2 class="today"><time class="timeago" datetime="{{ site.data.newnews.news[0].date }}">{{ site.data.newnews.news[0].date }}</time>, {{ site.data.newnews.news[0].date | date: "%A, %B %e, %Y" }}</h2>
<ul class="today">
{% for today in site.data.newnews.news[0].todays %}
 <li>{{ today.item }} <span class="small">{% if today.source != null %}(Source: <a href="{{ today.url }}">{{ today.source }}</a>){% endif %}</span></li>
{% endfor %}
  </ul>

<p class="outtro"><b>What's coming next:</b> {{ site.data.newnews.news[0].tomorrow }}</p>





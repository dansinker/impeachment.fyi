---
layout: home
---
<div id="archive">
  <h2>The impeachment happened. Here's all of it.</h2>
  <ul>
      {% assign sorted = (site.data.news.news | sort: 'news.date') | reverse %}
      {% for item in sorted %}
    <h3>{{ item.date | date: "%A, %B %d, %Y" }}</h3>
    <ul>
        {% for today in item.todays %}
         <li>{{ today.item }} <span class="small">{% if today.source != null %}<a href="{{ today.url }}">(Source: {{ today.source }})</a>{% endif %}</span></li>
        {% endfor %}
  </ul>
    {% endfor %}
</ul>
</div>
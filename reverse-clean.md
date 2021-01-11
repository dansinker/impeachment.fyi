---
layout: none
---
<div>
      {% assign sorted = (site.data.news.news | sort: 'news.date') | reverse %}
      {% for item in sorted %}
    <h3>{{ item.date | date: "%A, %B %d, %Y" }}</h3>
        {% for today in item.todays %}
         <p>{{ today.item }} <span class="small">{% if today.source != null %}<a href="{{ today.url }}">(Source: {{ today.source }})</a>{% endif %}</span></p>
        {% endfor %}
    {% endfor %}
</div>
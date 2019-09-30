---
layout: home
---
<div id="archive">
  <h2>Things happen fast. Here's all of it</h2>
  <div class="list">
    {% for new in site.data.news.news %}
    <div id="{{ new.date | date: "%Y-%m-%d" }}"></div>
      <p class="poops">On {{ new.date | date: "%B %-d, %Y" }}, the following happened:</p>
      <ul class="today">
        {% for today in new.todays %}
         <li>{{ today.item }} <span class="small"><a href="{{ today.url }}">(Source: {{ today.source }})</a></span></li>
        {% endfor %}
  </ul>
    {% endfor %}
  </div>
</div>

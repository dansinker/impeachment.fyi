---
layout: home
---
<div id="archive">
  <h2>Things happen fast. Here's all of it</h2>
  <div class="list">
    {% assign current_week = site.time | date: "%W" | plus: 0 %}
    {% capture filtered_dates_array %}
      {% for item in site.data.news.news %}
        {{ item.date | date: "%W" | plus: 0}}
      {% endfor %}
    {% endcapture %}
    {% assign weeks_array = filtered_dates_array | split: ' ' | uniq | join: ' '  %}
    {% assign weeks = weeks_array | split: ' '%}
    {% for week in weeks %}
    {% assign week_num = current_week | minus:week | plus:1 %}
      {% if week_num == 1 %}
        <h3>This Week</h3>
        {% for new in site.data.news.news %}
          {% assign news_week = new.date | date: "%W" | plus: 0 %}  
          {% if current_week == news_week %}
            <div>
              <h4>{{ new.date | date: "%B %-d, %Y" }}</h4>
            </div>
          {% endif %}
        {% endfor %}
      {% else %}
      <h3>Week {{week_num}}</h3>
      {% for new in site.data.news.news %}
          {% assign news_week = new.date | date: "%W" | plus: 0 %}
          {% assign week_dif = current_week | minus: news_week | plus:1 %}  
          {% if week_dif == week_num %}
            <div>
              <h4>{{ new.date | date: "%B %-d, %Y" }}</h4>
            </div>
          {% endif %}
        {% endfor %}

      {% endif %}
    {% endfor %}
  </div>
</div>

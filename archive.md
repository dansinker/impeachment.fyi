---
layout: home
---
<div id="archive">
  <h2>Things happen fast. Here's all of it</h2>
  <div class="list">
    {% assign current_week = site.time | date: "%U" | plus: 0 %}
    {% capture filtered_dates_array %}
      {% for item in site.data.news.news %}
        {{ item.date | date: "%U" | plus: 0}}
      {% endfor %}
    {% endcapture %}
    {% assign weeks_array = filtered_dates_array | split: ' ' | uniq | join: ' '  %}
    {% assign weeks = weeks_array | split: ' '%}
    {% for week in weeks %}
      {% assign week_week = week | plus: 0 %}
      {% if current_week < week_week %}
        {% assign current_week = current_week | plus: 52 %}
      {% endif %}
      {% assign week_num = current_week | minus: week | plus: 0 %}
      {% if week_num == 0 %}
        <section class="week">
          <h3>This Week</h3>
          {% for new in site.data.news.news %}
            {% include archive-article.html new=new if_week=current_week %}
          {% endfor %}
        </section>
      {% else %}
        <section class="week">
          {% if week_num == 1 %}
            <h3>Last Week</h3>
          {% else %}
            <h3>{{week_num}} Weeks Ago</h3>
          {% endif %}
          {% for new in site.data.news.news %}
            {% include archive-article.html new=new if_week=week %}
          {% endfor %}
        </section>
      {% endif %}
    {% endfor %}
  </div>
</div>

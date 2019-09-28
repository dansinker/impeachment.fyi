---
layout: home
---
<div id="archive">
{% assign counter = 0 %}
{% assign NJcount = 0 %}
{% for poop in site.data.trumps.poops %}
 {% assign counter = counter | plus: 1  %}
{% endfor %}
  <h2>💩 Trump has pooped {{ counter }} times since taking office 💩</h2>
  <div class="list">
    {% for poop in site.data.trumps.poops %}
      <p class="poops">On {{ poop.date | date: "%B %-d, %Y" }}, Trump pooped at <b>{{ poop.location }}</b> in {{ poop.city }}. <a href="{{ poop.link }}">[source]</a></p>
    {% endfor %}
  </div>
  <p style="text-align: center; margin-top: 50px"><small>The 💩 archive is available in <a href="https://github.com/sinker/trumppoopwatch.org/blob/master/_data/trumps.yml">machine-readable format on Github</a></small></p>
</div>

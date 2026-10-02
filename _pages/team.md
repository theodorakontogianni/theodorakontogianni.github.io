---
layout: page
permalink: /team/
title: Team
nav: true
nav_order: 2
---

{% assign groups = site.data.team | group_by: "category" %}
{% for group in groups %}
<section class="team-section" aria-labelledby="team-{{ group.name | slugify }}">
  <h2 id="team-{{ group.name | slugify }}">{{ group.name | escape }}</h2>
  <div class="team-grid">
    {% for member in group.items %}
    <div class="team-member">
      {% if member.image %}
      <img class="team-portrait" src="{{ member.image | relative_url }}" alt="{{ member.name | escape }}" width="160" height="160" loading="lazy">
      {% else %}
      <div class="team-portrait team-initial" aria-hidden="true">{{ member.name | slice: 0 | upcase }}</div>
      {% endif %}
      <h3>{% if member.url %}<a href="{{ member.url | relative_url }}">{{ member.name | escape }}</a>{% else %}{{ member.name | escape }}{% endif %}</h3>
      {% if member.co_supervisor %}
      <p class="team-supervision">Co-supervised with <a href="{{ member.co_supervisor.url | escape }}">{{ member.co_supervisor.name | escape }}</a></p>
      {% elsif member.supervision %}
      <p class="team-supervision">{{ member.supervision | escape }}</p>
      {% endif %}
    </div>
    {% endfor %}
  </div>
</section>
{% endfor %}

<section class="team-join">
  <h2>Join our team</h2>
  <p>We are looking for motivated PhD students and postdoctoral researchers
  interested in 3D vision and 3D perception.</p>
  <a href="mailto:thekon@dtu.dk">Get in touch <span aria-hidden="true">&rarr;</span></a>
</section>

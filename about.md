---
layout: default
title: About
---

# About The Commoner Archive

This is a shared notebook. Everything on it was written by someone in our
friend group and handed over to be posted here — no strangers, no algorithm
deciding what rises to the top, just things we wanted each other to read.

Want to contribute something? Send your article over in .txt format at thecommonerarchive@gmail.com

## Who writes here

<div class="contributors-list">
{% for c in site.data.contributors %}
  <div class="contributor-card">
    <span class="badge" style="background-color: {{ c[1].color | default: '#8C8577' }}">
      {{ c[1].initials | default: c[0] | slice: 0, 2 | upcase }}
    </span>
    <div>
      <p class="contributor-name">
        {% if c[1].archive %}<a href="{{ c[1].archive | relative_url }}">{{ c[0] }}</a>{% else %}{{ c[0] }}{% endif %}
      </p>
      {% if c[1].bio %}<p class="contributor-bio">{{ c[1].bio }}</p>{% endif %}
    </div>
  </div>
{% endfor %}
</div>

---
layout: base.njk
---


{% for item in test.data %}
# {{ item.name }}
{{ item.description }}

Appearences:
{% for game in games.data %}
{% for id in item.games %}
{% if game._id == id %}
{{ game.name }}
{% endif %}
{% endfor %}

{% endfor %}


{% endfor %}

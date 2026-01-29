---
layout: default
subnav: fmics
---

## Invited Speakers FMICS

{% assign speakers = site.speakers | sort_natural: 'last_name' %}

{% for speaker in speakers %}
    {% if speaker.conference == "FMICS" %}
  ---
  <div style="background-color:rgba(0, 0, 0, 0.0470588); text-align:left; vertical-align: middle; padding:40px 20px;">
    <h3>{{ speaker.first_name }} {{ speaker.last_name }}</h3>
    {{ speaker.affiliation }}<br/>      
    {% if speaker.atitle %}<h3>{{ speaker.atitle }}</h3>{% endif %}
    <p><a href="{{ "/assets/images/" | relative_url }}{{ speaker.img }}">
      <img src="{{ "/assets/images/" | relative_url }}{{ speaker.img }}" alt="{{ speaker.full_name: }}" style="float:right; padding:0 10px; width:30%">
    </a>
    {% if speaker.abstract %}{{ speaker.abstract }}{% endif %}
    {% if speaker.bio %}<h3>Bio</h3>{% endif %}
    {% if speaker.bio %}{{ speaker.bio }}{% endif %}
    </p>
  </div>
    {% endif %}
{% endfor %}

---

## Joint CONFEST Invited Speakers 

{% assign speakers = site.speakers | sort_natural: 'last_name' %}

{% for speaker in speakers %}
    {% if speaker.joint %}
  ---
  <div style="background-color:rgba(0, 0, 0, 0.0470588); text-align:left; vertical-align: middle; padding:40px 20px;">
    <h3>{{ speaker.first_name }} {{ speaker.last_name }}</h3>
    {{ speaker.affiliation }}<br/>      
    {% if speaker.atitle %}<h3>{{ speaker.atitle }}</h3>{% endif %}
    <p><a href="{{ "/assets/images/" | relative_url }}{{ speaker.img }}">
      <img src="{{ "/assets/images/" | relative_url }}{{ speaker.img }}" alt="{{ speaker.full_name: }}" style="float:right; padding:0 10px; width:30%">
    </a>
    {% if speaker.abstract %}{{ speaker.abstract }}{% endif %}
    <h3>Bio</h3>
    {% if speaker.bio %}{{ speaker.bio }}{% endif %}
    </p>
  </div>
    {% endif %}
{% endfor %}

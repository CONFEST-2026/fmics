---
layout: default
subnav: fmics
---
 
 
# FMICS 2026

<section class="section">
<div class="grid23">
<div class="card" markdown=1>

The aim of the **FMICS** conference series is to provide a forum for researchers and practitioners who are interested in the development and application of formal methods in industry. FMICS brings together scientists and engineers who are active in the area of formal methods and interested in exchanging their experiences in the industrial usage of these methods. The FMICS conference series also strives to promote research and development for the improvement of formal methods and tools for industrial applications.

FMICS is the [**ERCIM** Working Group][ERCIM] conference on Formal Methods for Industrial Critical Systems, and it is the key conference in the intersection of industrial applications and Formal Methods.
</div>
<div class="card" markdown=1 >
##### Important dates

- *Abstracts:*       ~~10 April, 2026~~ 24 April, 2026
- *Submissions:*     ~~17 April, 2026~~ 1 May, 2026
- *Notification:*    1 June, 2026
- *Camera Ready:*    15 June, 2026
- *Conference:*      2 -- 4 September, 2026
- *Workshops:*       5 September, 2026
</div>
</div>
</section>



---


##### FMICS Invited Speakers

{% assign speakers_concur = site.speakers | where: "conference", "FMICS" %}
{% assign speakers_all = site.speakers | where: "conference", "all" %}

{% assign speakers = speakers_concur | concat: speakers_all 
  | where: "invited", true 
  | sort_natural: "last_name" %}


<div class="card-deck mt-4">
  {% for speaker in speakers %}
      {% assign website = speaker.links | first %}
    <div class="card">
      <img class="card-img-top" 
      src="{{ "/assets/images/" | relative_url }}{{ speaker.img }}.webp" alt="{{ speaker.full_name }}">
      <div class="card-body">
          <h5 class="card-title">{{ speaker.first_name }} {{ speaker.last_name }}</h5>
          {% if speaker.extra %}<p class="card-text">{{ speaker.extra }}</p>{% endif %}
          {% if speaker.short_affiliation %}<p class="card-text small">{{ speaker.short_affiliation }}</p>{% endif %}
                  <a href="{{ speaker.url }}" class="stretched-link"></a>
                  <p class="small">
			          {% if speaker.conference == 'all' %}
			          Joint CONFEST Speaker
			          {% else %}
			          {{speaker.conference}} Speaker
			          {% endif %}
			      </p>
      </div>
    </div>
  {% endfor %}
</div>

---

##### Awards


Following FMICS tradition, the paper with the best contributions to Software Science and Technology will be honoured with the EASST ERCIM award.

---


##### Contact


For questions please contact the PC chairs via <mailto:fmics2026@easychair.org>.

[COH]: https://www.drisq.com/about
[JB]: https://www.nasa.gov/johnson/
[ERCIM]: https://fmics.inria.fr/
[KYR]: https://www.aere.iastate.edu/kyrozier/
[PGL]: https://pure.au.dk/portal/en/persons/pgl@ece.au.dk


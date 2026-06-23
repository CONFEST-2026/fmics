---
title: Accepted Papers
layout: default
subnav: fmics
---

# {{page.title}}

<ul>
    {% for paper in site.data.fmics-accepted-papers %}
        <li>
            <strong>{{ paper.Authors }}</strong>. {{ paper.Title }}
        </li>
    {% endfor %}
</ul>

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

## Best Paper Awards

Congratulations to:

- Ian J. Hayes, Larissa Meinicke and Cliff Jones, Reasoning about concurrent loops and recursion with rely-guarantee rules. (Best Paper and EASST ERCIM award)

- Alessandro Fantechi, Gloria Gori and Jacopo Zecchi, Exploiting the Layout of a Railway Interlocking System for Path Reliability Evaluation (Best Paper award)

---
title: Tutkimusseuranta
permalink: /tutkimukset/
description: Yhteenvedot tuottavuustutkimuksista Tuottavuuslautakunnan näkökulmasta
---

# Tutkimusseuranta

<p class="lede">Yhteenvedot tuoreista tuottavuustutkimuksista. Jokainen yhteenveto noudattaa samaa kuuden kohdan rakennetta: tutkimuksen tiedot, yhteenveto, Suomi tutkimuksessa, sovellettavuus Suomeen, suhde Tuottavuuslautakunnan raportteihin sekä jatkotutkimuskysymykset. Ks. <a href="{{ '/menetelma/' | relative_url }}">menetelmä</a>.</p>

{% assign tutkimukset = site.tutkimukset | sort: 'julkaistu' | reverse %}
{% if tutkimukset.size == 0 %}
<p>Ei vielä yhteenvetoja.</p>
{% else %}
<ul class="cards">
{% for t in tutkimukset %}
  <li class="card">
    <h3><a href="{{ t.url | relative_url }}">{{ t.title }}</a></h3>
    <p class="small">{{ t.julkaisija }}{% if t.julkaistu %} · {{ t.julkaistu | date: '%-d.%-m.%Y' }}{% endif %}{% if t.tyyppi %} · {{ t.tyyppi }}{% endif %}</p>
    {% if t.alaotsikko %}<p>{{ t.alaotsikko }}</p>{% endif %}
    {% if t.tlk_arvio %}<p class="small"><strong>TLK-näkökulma:</strong> {{ t.tlk_arvio }}</p>{% endif %}
    {% if t.teemat %}<ul class="tags">{% for x in t.teemat %}<li>{{ x }}</li>{% endfor %}</ul>{% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}

## Teemoittain

{% assign kaikki = "" | split: "" %}
{% for t in site.tutkimukset %}{% for x in t.teemat %}{% assign kaikki = kaikki | push: x %}{% endfor %}{% endfor %}
{% assign teemat = kaikki | uniq | sort %}
{% for teema in teemat %}{% assign osumat = tutkimukset | where_exp: "t", "t.teemat contains teema" %}
**{{ teema }}:** {% for t in osumat %}[{{ t.title }}]({{ t.url | relative_url }}){% unless forloop.last %} · {% endunless %}{% endfor %}
{% endfor %}

## Ehdota tutkimusta

Uuden yhteenvedon voi tehdä Claude Codella tämän repositorion skillillä `tutkimusanalyysi`: anna tutkimuksen linkki ja pyydä analyysi. Ohje on tiedostossa [`.claude/skills/tutkimusanalyysi/SKILL.md`](https://github.com/tuottavuuslautakunta/tutka/blob/main/.claude/skills/tutkimusanalyysi/SKILL.md).

---
title: Etusivu
permalink: /
---

# Tutka

<p class="lede">Tuottavuustutkimuksen seuranta Tuottavuuslautakunnan näkökulmasta. Sivusto kokoaa lautakunnan raporttien keskeiset havainnot ja suositukset ja suhteuttaa niihin uusia kotimaisia ja kansainvälisiä tuottavuustutkimuksia.</p>

<p class="ai-note"><strong>Huom.</strong> Sivuston yhteenvedot sekä lautakunnan raporteista että tutkimuksista on tehty tekoälyn (Claude) avulla. Ne ovat apuväline seurantaan, eivät virallisia kannanottoja – tarkista luvut aina alkuperäisestä julkaisusta.</p>

<ul class="cards">
  <li class="card">
    <h3><a href="{{ '/raportit/' | relative_url }}">Lautakunnan raportit 2019–2026</a></h3>
    <p>Seitsemän vuosiraportin ja vuoden 2026 suositusten tiivistelmät linkkeineen sekä raporteissa toistuvat linjaukset teemoittain.</p>
  </li>
  <li class="card">
    <h3><a href="{{ '/tutkimukset/' | relative_url }}">Tutkimusseuranta</a></h3>
    <p>Yhteenvedot uusista tutkimuksista kuuden kohdan rakenteella: mitä tutkimus sanoo, koskeeko se Suomea, miten se sopii lautakunnan havaintoihin ja mitä jatkokysymyksiä siitä nousee.</p>
  </li>
  <li class="card">
    <h3><a href="{{ '/menetelma/' | relative_url }}">Menetelmä</a></h3>
    <p>Miten tutkimukset analysoidaan ja miten uuden yhteenvedon voi lisätä.</p>
  </li>
</ul>

## Uusimmat tutkimusyhteenvedot

{% assign uusimmat = site.tutkimukset | sort: 'julkaistu' | reverse %}
{% for t in uusimmat limit: 5 %}
- [{{ t.title }}]({{ t.url | relative_url }}) – {{ t.julkaisija }}, {{ t.julkaistu | date: '%-d.%-m.%Y' }}  
  <span class="small">{{ t.tlk_arvio }}</span>
{% endfor %}

## Lautakunnan uusin linja lyhyesti

Tuottavuuslautakunnan [vuosiraportti 2026](https://urn.fi/URN:ISBN:978-952-367-587-2) ja [suositukset](https://urn.fi/URN:ISBN:978-952-367-591-9) julkaistiin 30.9.2026. Niiden keskeiset viestit:

- **Ero verrokkeihin.** Yrityssektorin työn tuottavuus on yhä lähes finanssikriisiä edeltävällä tasolla, eikä ero verrokkimaihin ole kaventunut.
- **Yksityiset palvelut.** Niiden heikko tuottavuus johtuu matalasta pääomaintensiteetistä, heikosta kohdentumisesta ja digiteknologian keskittymisestä harvoille yrityksille.
- **Julkinen tuki.** Säilyttäviä yritystukia karsitaan, ja tuella korjataan markkinapuutteita.
- **Kilpailu.** Kilpailupolitiikalla vahvistetaan markkinoiden uudistumista.
- **Osaaminen.** Perusopetuksen oppimistulokset käännetään nousuun.
- **Julkinen sektori.** Tuottavuuspolitiikka perustuu tuotosten laadun ja vaikuttavuuden mittaamiseen, ei tilinpidon kokonaislukuihin.

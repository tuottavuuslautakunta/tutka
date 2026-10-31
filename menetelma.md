---
title: Menetelmä
permalink: /menetelma/
---

# Miten tutkimukset analysoidaan

Jokainen tutkimusyhteenveto tehdään samalla rakenteella, jotta ne ovat keskenään vertailukelpoisia ja helposti suhteutettavissa Tuottavuuslautakunnan työhön. Rakenne on määritelty repositorion skillissä [`tutkimusanalyysi`](https://github.com/tuottavuuslautakunta/tutka/blob/main/.claude/skills/tutkimusanalyysi/SKILL.md), jota Claude Code käyttää yhteenvetoja laatiessaan.

| # | Osio | Sisältö |
|---|------|---------|
| 1 | Tutkimuksen tiedot | Nimi, tekijät, julkaisija, päivämäärä, tyyppi, linkki, aineisto ja menetelmä. |
| 2 | Yhteenveto | Ydinviesti, keskeiset tulokset, menetelmän uskottavuus ja rajoitukset. |
| 3 | Suomi tutkimuksessa | Jos tutkimus ei ole Suomi-spesifi: onko Suomi mukana ja millaisin tuloksin. |
| 4 | Sovellettavuus Suomeen | Rakenteelliset erot, toistettavuus suomalaisella datalla, politiikkajohtopäätökset. |
| 5 | Suhde TLK:n raportteihin | Onko aihetta käsitelty lautakunnan raporteissa; tukeeko, täydentääkö vai haastaako tutkimus lautakunnan havaintoja ja suosituksia. |
| 6 | Jatkotutkimuskysymykset | Mitä avoimia kysymyksiä tutkimuksesta nousee Suomen ja lautakunnan kannalta. |

## Tekoälyn käyttö

Kaikki sivuston yhteenvedot – sekä [Tuottavuuslautakunnan raporttien tiivistelmät]({{ '/raportit/' | relative_url }}) että [tutkimusyhteenvedot]({{ '/tutkimukset/' | relative_url }}) – on tehty tekoälyn (Anthropicin Claude) avulla:

- Raporttien tiivistelmät on laadittu raporttien PDF-versioista ja niistä aiemmin tehdystä raporttikatsauksesta.
- Tutkimusyhteenvedot laaditaan skillillä `tutkimusanalyysi`, joka määrittää analyysin rakenteen, lähteiden käytön ja tarkistuslistan. Jokaisen yhteenvedon metatiedoissa kerrotaan, perustuuko analyysi kokotekstiin vai pelkkään tiivistelmään.
- Kohtien 4 (sovellettavuus Suomeen), 5 (suhde lautakunnan raportteihin) ja 6 (jatkotutkimuskysymykset) arviot ovat tekoälyn tulkintoja, eivät Tuottavuuslautakunnan kannanottoja.

Tekoälyn tuottama teksti voi sisältää virheitä, puutteita tai painotuksia, joita alkuperäisissä julkaisuissa ei ole. Yhteenvedot on tarkoitettu seurannan apuvälineeksi.

## Periaatteet

- Luvut ja maavertailut raportoidaan vain sellaisina kuin ne lähteessä esitetään. Jos analyysi perustuu pelkkään tiivistelmään, se kerrotaan sivulla.
- Tutkimuksen omat väitteet ja tämän sivuston arviot erotetaan toisistaan.
- Vertailukohtana käytetään [Tuottavuuslautakunnan raporttien yhteenvetoa]({{ '/raportit/' | relative_url }}).
- Yhteenvedot ovat tiivistelmiä: tarkista aina alkuperäinen julkaisu ennen lainaamista.

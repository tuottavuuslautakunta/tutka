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

## Lautakunnan uusin raportti

Tuottavuuslautakunta julkaisi 30.9.2026 [vuosiraportin 2026](https://urn.fi/URN:ISBN:978-952-367-587-2) (VM 2026:40) ja [suositukset 2026](https://urn.fi/URN:ISBN:978-952-367-591-9) (VM 2026:41). Alla julkaisujen tiivistelmät kuvailulehdiltä.

### Vuosiraportti 2026: Palvelusektorin tuottavuus, yritysten uudistuminen ja kilpailun tila

Suomen talouden kasvu on ollut selvästi verrokkimaita hitaampaa, ja ongelmana on ollut työn tuottavuuden heikko kasvu. Yrityssektorin tuottavuus oli vuonna 2025 edelleen lähes samalla tasolla kuin lähes 20 vuotta sitten. Suomen talouden suhteellinen kustannuskilpailukyky on lähellä pitkän aikavälin keskiarvoa. Kustannuskilpailukykyä on pitänyt yllä heikon tuottavuuskasvun oloissa verrokkimaita heikompi palkkakehitys.

Raportti tarkastelee erityisesti palveluiden tuottavuutta. Yksityisten palveluiden tuottavuus on heikkoa verrokkimaihin nähden. Tälle ei ole yksittäistä syytä. Suomessa palvelualoilla pääomaa on verrokkimaita vähemmän. Pääoma ja osaava työvoima ei kohdistu tehokkaimmalla tavalla. Digitaalisen teknologian hyödyntäminen on keskittynyt pienelle joukolle yrityksiä. Korkean teknologian aloilla on nopeasti kasvavia tuottavia yrityksiä, mutta ne ovat edelleen pääosin pieniä. Viime vuosina ”luova tuho” on vauhdittanut tuottavuuskasvua. Samaan aikaan markkinat ovat keskittyneet, markkinoille tulevien yritysten määrä on vähentynyt ja suurten yritysten pysyvyys markkinoilla on kasvanut.

Julkisten palveluiden tuottavuutta ei voi mitata samalla tavalla kuin yksityisen sektorin tuottavuutta. Mittaamiseen liittyvät ongelmat eivät kuitenkaan tarkoita, ettei tuottavuuden mittaamiselle olisi tarvetta. Päinvastoin mittaamisen ja vaikutusarvioiden kehittäminen ja laajentaminen ovat edellytys tuottavuuden parantamiselle ja oikeanlaisten kannustimien luomiselle palveluiden kehittämiseksi.

### Suositukset 2026

**Julkisen tuen tulee korjata markkinapuutteita.** Säilyttäviä yritystukia tulisi karsia ja kohdentaa tuet vaikuttavammin. Koulutuksen ja tutkimuksen tukeminen on perusteltua, investointien ja innovaatioiden tukeminen yleensä ei. Verotus ei saisi suosia tiettyjä yhtiömuotoja, pääomatyyppejä tai yrityskokoja. Esimerkiksi listaamattomien yritysten osinkoverotus vääristää pääoman kohdentumista.

**Markkinoiden uudistumiskykyä tulee voimistaa kilpailupolitiikalla.** Hyvin toimiva kilpailu markkinoilla lisää innovaatiota sekä kiihdyttää tuottavuutta vahvistavaa rakennemuutosta. Kilpailuviranomaiselle tulisi antaa mahdollisuus tutkia myös ilmoituskynnyksen alittavia yrityskauppoja. Kilpailukieltosopimuksia ja ammattipätevyysvaatimuksia rajoittamalla voitaisiin lisätä työpaikan vaihtoja ja osaamisen leviämistä. Lainvalmistelussa olisi arvioitava vaikutukset kilpailuun.

**Osaamistason vahvistaminen on tuottavuuden kannalta keskeistä.** Perusopetuksen osaamiskehitys on käännettävä nousuun, ja huomio tulee kohdistaa resurssien määrän ohella oppimistuloksiin ja toimiviksi osoitettujen käytäntöjen levittämiseen. Tämä edellyttää valtakunnallista oppimistulosten mittaamista ja rekisteriä. Yliopistojen perustutkimus luo perustan innovaatioille ja uusien teknologioiden käyttöönotolle.

**Julkisella sektorilla tuottavuuspolitiikan tulee perustua tuotosten laadun ja vaikuttavuuden mittaamiseen, tutkimukseen ja kannusteisiin.** Tuottavuutta ja vaikuttavuutta parantavia tavoitteita ja kannusteita ei voida asettaa, jos mittarit eivät kuvaa niitä oikein. Uudistuksia kannattaa ensin kokeilla pienessä mittakaavassa.

Tarkempi yhteenveto kaikista lautakunnan raporteista on [raporttisivulla]({{ '/raportit/' | relative_url }}).

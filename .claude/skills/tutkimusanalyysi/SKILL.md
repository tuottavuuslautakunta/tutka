---
name: tutkimusanalyysi
description: Tekee Tutka-sivustolle (tuottavuustutkimuksen seuranta) uuden tutkimusyhteenvedon Tuottavuuslautakunnan näkökulmasta. Käytä, kun käyttäjä antaa linkin, DOI:n tai PDF:n tuottavuutta käsittelevään tutkimukseen, raporttiin tai working paperiin ja pyytää analyysiä, yhteenvetoa tai sen lisäämistä sivustolle; myös kun pyydetään päivittämään olemassa olevaa yhteenvetoa tai vertaamaan tutkimusta lautakunnan raportteihin.
---

# Tutkimusanalyysi Tutka-sivustolle

Tavoite: tuottaa yksi Markdown-tiedosto `_tutkimukset/`-kansioon. Tiedosto kertoo päätöksentekijälle ja
virkamiehelle lyhyesti, mitä tutkimus sanoo, koskeeko se Suomea ja miten se suhteutuu Tuottavuuslautakunnan
(jäljempänä TLK) havaintoihin ja suosituksiin. Kieli on suomi, sävy asiallinen ja virkamiesmäinen, ei mainoksellinen.

## Työvaiheet

1. **Hae tutkimus.** Lue koko teksti, jos mahdollista (PDF, HTML, DOI → julkaisijan sivu, RePEc/IDEAS, SSRN,
   NBER, CEPR, ETLA/VATT/Palkansaajien tutkimuslaitos, Suomen Pankki/BoF). Jos vain tiivistelmä on saatavilla,
   tee analyysi silti, mutta merkitse se front matteriin (`lahdepohja: "Tiivistelmä – kokoteksti ei saatavilla"`)
   ja kirjoita kohdat 2–3 varovasti. **Älä koskaan keksi lukuja, maita tai tuloksia, joita lähteessä ei ole.**
2. **Lue lautakunnan linja.** Avaa `raportit.md` (raporttien yhteenvedot ja läpileikkaavat teemat).
   Tarvittaessa tarkista yksityiskohta itse raportista sivulla olevasta urn.fi-linkistä.
3. **Kirjoita tiedosto** alla olevalla rakenteella. Tiedostonimi:
   `_tutkimukset/VVVV-KK-PP-lyhyt-tunniste.md`, jossa päivämäärä on tutkimuksen julkaisupäivä
   (tai kuukauden 1. päivä, jos vain kuukausi tiedossa) ja tunniste on 2–5 sanaa pienillä kirjaimilla ja viivoilla.
4. **Tarkista** (ks. tarkistuslista lopussa), aja `jekyll build` jos saatavilla, ja kerro käyttäjälle tiivis
   yhteenveto sekä mahdolliset epävarmuudet.

## Front matter

```yaml
---
title: "Tutkimuksen nimi alkuperäiskielellä"
alaotsikko: "Yhden virkkeen suomenkielinen kuvaus siitä, mistä on kyse"
tekijat: ["Etunimi Sukunimi", "Etunimi Sukunimi"]
julkaisija: "OECD"                 # organisaatio tai lehti
sarja: "Economics Department Working Papers No. 1878"   # valinnainen
julkaistu: 2026-10-23
tyyppi: "Working paper"            # Working paper | Vertaisarvioitu artikkeli | Raportti | Selvitys | Policy brief
maantiede: "OECD-maat"             # esim. "Suomi", "EU-27", "Yhdysvallat", "OECD-maat"
suomi: "Ei erillistä Suomi-analyysiä"   # Kyllä – oma analyysi | Mukana vertailussa | Ei erillistä Suomi-analyysiä | Ei mukana | Ei varmistettu
linkki: "https://..."
doi: "10.xxxx/xxxx"                # valinnainen, ilman https://doi.org/
teemat: ["julkinen sektori", "mittaaminen"]   # käytä alla olevaa teemasanastoa
tlk_raportit: [2026, 2023]         # TLK:n raporttien vuodet, joissa aihetta käsitelty
tlk_arvio: "Tukee ..."             # yksi virke: tukee / täydentää / haastaa / ei kosketuskohtaa
analysoitu: 2026-10-28
lahdepohja: "Kokoteksti"           # tai "Tiivistelmä – kokoteksti ei saatavilla"
---
```

**Teemasanasto** (pidä yhtenäisenä, jotta suodatus toimii): `julkinen sektori`, `mittaaminen`,
`palvelut`, `teollisuus`, `kilpailu`, `yritysdynamiikka`, `T&K ja innovaatiot`, `digitalisaatio ja tekoäly`,
`osaaminen ja koulutus`, `työmarkkinat`, `investoinnit ja pääoma`, `kansainvälinen kauppa`,
`vihreä siirtymä`, `yritystuet`, `sääntely`, `alueet`, `makrotalous`. Lisää uusi teema vain, jos mikään ei sovi.

## Sisältö – viisi pakollista osiota

Käytä täsmälleen näitä otsikoita (h2), jotta sivut ovat vertailukelpoisia.

### `## 1. Tutkimuksen tiedot`
Lyhyt taulukko tai lista: nimi, tekijät, julkaisija/sarja, julkaisupäivä, tyyppi, kieli, linkki (ja DOI),
aineisto ja ajanjakso, menetelmä yhdellä rivillä. Mainitse, jos kyse on luonnoksesta tai vertaisarvioimattomasta työstä.

### `## 2. Yhteenveto tutkimuksesta`
- Aloita 2–3 virkkeen **ydinviestillä** (mitä tutkimus väittää ja miksi sillä on merkitystä).
- Sitten **keskeiset tulokset** 3–7 luettelokohtana, luvut mukaan sellaisina kuin lähteessä.
- **Menetelmä ja aineisto** lyhyesti; arvioi identifikaation uskottavuus (kausaalinen vai kuvaileva).
- **Rajoitukset**: mitä tutkimus ei kerro.
Pituus noin 250–450 sanaa.

### `## 3. Suomi tutkimuksessa`
- Jos tutkimus on Suomi-spesifi: kirjoita "Tutkimus koskee Suomea" ja siirry kohtaan 4 (voit tiivistää).
- Muuten: onko Suomi aineistossa? Raportoi Suomen tulokset ja sijoitus verrokkimaihin (erityisesti
  Ruotsi, Tanska, Alankomaat, Saksa, Yhdysvallat – TLK:n vakioverrokit) täsmälleen lähteen mukaan.
- Jos Suomea ei käsitellä, sano se suoraan ja kerro, onko Suomesta saatavilla vastaavaa dataa
  (esim. Tilastokeskus, Findicator, OECD:n tietokannat).

### `## 4. Sovellettavuus Suomeen`
Arvioi, miten tulokset siirtyvät Suomeen. Käy läpi ainakin:
- **Rakenteelliset erot**: elinkeinorakenne, julkisen sektorin koko ja organisointi (hyvinvointialueet,
  kunnat), työmarkkinainstituutiot, yrityskoko, avoimuus.
- **Data ja mittaaminen**: voidaanko tulos toistaa suomalaisella aineistolla (Tilastokeskuksen
  yritys- ja työntekijätason rekisteriaineistot, FOLK, kansantalouden tilinpito)?
- **Politiikkajohtopäätökset**: mitä Suomessa voitaisiin tehdä toisin, kuka (ministeriö/virasto).
Päätä yhdellä virkkeellä: sovellettavuus *hyvä / kohtalainen / rajallinen* ja miksi.

### `## 5. Suhde Tuottavuuslautakunnan raportteihin`
- **Onko aihetta käsitelty?** Luettele raportit vuosineen ja linkkeineen (linkit `raportit.md`:stä), joissa
  aihe esiintyy, ja mitä TLK siitä sanoi.
- **Yhteensopivuus**: tukeeko tutkimus TLK:n havaintoja, näkemyksiä tai suosituksia, täydentääkö se niitä
  (uusi näkökulma tai aineisto) vai haastaako se ne? Perustele konkreettisesti.
- **Aukot**: jos TLK ei ole käsitellyt aihetta, sano se ja arvioi, kannattaisiko sen tulla lautakunnan
  agendalle.
- Tiivistä lopuksi front matterin `tlk_arvio`-kenttään yhteen virkkeeseen.

Lopuksi valinnainen `## Lisälukemista` -osio (enintään 5 linkkiä, vain varmistettuja).

## Tyyli

- Suomeksi; vakiintuneet termit: *työn tuottavuus*, *kokonaistuottavuus (TFP)*, *kansantalouden tilinpito*,
  *volyymi*, *laatukorjattu tuotos*, *hyvinvointialueet*. Englanninkielinen termi sulkuihin ensimmäisellä kerralla,
  jos käännös ei ole vakiintunut.
- Erota selvästi, mikä on **tutkimuksen** väite ja mikä on **tämän analyysin** arvio (esim. "Arviomme mukaan …").
- Ei liioittelua; epävarmuus ääneen. Lainaukset lyhyitä ja lähteeseen sidottuja.
- Linkit aina täydellisinä URL-osoitteina; älä keksi linkkejä.

## Tarkistuslista ennen tallennusta

- [ ] Front matter täydellinen, `julkaistu` ja `analysoitu` muodossa VVVV-KK-PP.
- [ ] Viisi osiota oikeilla otsikoilla ja oikeassa järjestyksessä.
- [ ] Jokainen luku ja maavertailu löytyy lähteestä; muuten poistettu tai merkitty "ei varmistettu".
- [ ] Kohdassa 5 viitatut TLK-raportit ovat olemassa `raportit.md`:ssä ja linkit toimivat.
- [ ] `lahdepohja` kertoo rehellisesti, perustuuko analyysi kokotekstiin.
- [ ] Jos uusi TLK-raportti on julkaistu, päivitä ensin `raportit.md` (ks. alla).

## TLK:n uuden raportin lisääminen

Kun Tuottavuuslautakunta julkaisee uuden raportin, lisää se `raportit.md`:n alkuun samalla rakenteella kuin
muut (otsikko, julkaisupäivä, linkit, pääteema, keskeiset havainnot, suositukset, teemat) ja päivitä
"Läpileikkaavat teemat" -osio. Tarkista sen jälkeen, muuttuuko jonkin aiemman tutkimusyhteenvedon kohta 5.

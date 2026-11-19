---
name: tutkimusseuranta
description: Viikoittainen tuottavuustutkimuksen seuranta Tutka-sivustolle. Hakee keskeisistä lähteistä edellisen ajon jälkeen julkaistut tuottavuutta käsittelevät tutkimukset, raportit ja työpaperit, karsii jo käsitellyt ja ehdottaa listaa lisättäviksi. Käytä ajastetussa viikkohaussa tai kun käyttäjä pyytää etsimään uusia tutkimuksia, ehdotuksia Tutkaan tai päivittämään seurantajonoa.
---

# Tutkimusseuranta Tutka-sivustolle

Tavoite: tuottaa kerran viikossa (perjantaisin) lyhyt, numeroitu **ehdotuslista** tuoreista tuottavuutta
käsittelevistä julkaisuista, joista käyttäjä valitsee analysoitavat. Tämä skill **ei kirjoita analyyseja**;
valitut julkaisut analysoidaan myöhemmin skillillä `tutkimusanalyysi`.

## Työvaiheet

1. **Selvitä aikaikkuna.** Katso uusin tiedosto `seuranta/ehdotukset/` -kansiosta. Hae julkaisut sen päivämäärästä
   (miinus 3 päivää päällekkäisyydeksi) tähän päivään. Jos aiempaa ajoa ei ole, käytä 14 päivää.
2. **Kokoa jo tunnetut.** Lue `_tutkimukset/`-tiedostojen otsikot ja linkit sekä `seuranta/jono.md`
   (aiemmin löydetyt, ei vielä valitut) ja `seuranta/hylatyt.md` (käyttäjän hylkäämät). Näitä ei ehdoteta
   uudelleen uusina. Jos jonossa olevalle julkaisulle on tullut uusi versio (esim. lehtiversio), sen voi mainita.
3. **Hae lähteistä** (alla). Käytä WebSearch- ja WebFetch-työkaluja (lataa ToolSearchilla
   "select:WebFetch,WebSearch") sekä tarvittaessa curlia. Tee haut rinnakkain.
4. **Rajaa ja pisteytä.** Ota mukaan vain julkaisut, jotka käsittelevät tuottavuutta tai sen keskeisiä ajureita
   ja jotka on julkaistu aikaikkunassa. Järjestä tärkeysjärjestykseen (kriteerit alla). Enintään 12 ehdotusta;
   jos relevantteja ei löydy, sano se.
5. **Varmista.** Jokaisen ehdotuksen nimi, tekijät, julkaisija, päivämäärä ja URL on tarkistettava
   hakutuloksesta tai sivulta. Älä keksi mitään; merkitse epävarma "ei varmistettu".
6. **Kirjoita** ehdotustiedosto `seuranta/ehdotukset/VVVV-KK-PP.md` (muoto alla) ja lisää ehdotukset
   `seuranta/jono.md`:n loppuun osioon kyseisellä päivämäärällä.
7. **Julkaise:** commitoi ja pushaa suoraan `main`-haaraan (hae ensin `origin/main`, varmista fast-forward).
   Kansio `seuranta/` ei näy sivustolla (`_config.yml` exclude).
8. **Tiivistelmä käyttäjälle:** lopeta viestiin, jossa on ehdotuslista (numero, nimi, julkaisija, yhden rivin
   perustelu) ja kehotus vastata numeroilla. Kun käyttäjä vastaa, tee valituista analyysit skillillä
   `tutkimusanalyysi` ja siirrä hylätyt (jos käyttäjä niin sanoo) `seuranta/hylatyt.md`:hen.

## Lähteet

Lähteet on koottu Tutkan alkuvaiheen hauista (11/2024–10/2026). Painota suomalaisia ja pohjoismaisia.

**Suomi**
- ETLA: raportit, muistiot, working papers – https://www.etla.fi/julkaisut/ (sivut ja PDF:t latautuvat suoraan)
- Labore (Palkansaajien tutkimuslaitos): https://labore.fi/julkaisut/
- VATT ja VATT Datahuone: https://vatt.fi/julkaisut ; Doria-arkisto https://doria.fi
- Suomen Pankki: BoF Bulletin https://www.bofbulletin.fi , Euro & talous https://www.eurojatalous.fi , BoF Economics Review
- PTT: https://www.ptt.fi/julkaisut/
- KKV:n tutkimusraportit: https://www.kkv.fi/tutkimus-ja-vaikuttaminen/julkaisut/
- Tilastokeskus: tuottavuustilastot (kasvu- ja tuottavuusmittarit) https://stat.fi
- Valtioneuvoston julkaisuarkisto Valto, TEAS-hankkeet: https://julkaisut.valtioneuvosto.fi (HTML voi palauttaa 403;
  käytä urn.fi-linkkejä tai hakukonetta)
- Talouspolitiikan arviointineuvosto, Sitra, Verotutkimuksen FIT (https://verotutkimus.fi), Kansantaloudellinen
  aikakauskirja (https://journal.fi/kak), Tutkimus- ja innovaationeuvosto

**Pohjoismaat**
- Ruotsi: Konjunkturinstitutet (https://www.konj.se), regeringen.se (SOU), Tillväxtanalys
- Tanska: De Økonomiske Råd (produktivitetsraportit, https://dors.dk), Nationalbanken
- Norja: SSB, Finansdepartementet (NOU), Norges Bank

**Kansainväliset järjestöt**
- OECD: Economics Department WP (https://ideas.repec.org/s/oec/ecoaaa.html), STI- ja Productivity WP,
  Compendium of Productivity Indicators, Economic Surveys (Suomi, Ruotsi, Tanska), Employment Outlook, Global Forum
  on Productivity. oecd.org palauttaa usein 403; käytä RePEc/IDEAS-sivuja ja oecd.org/content/dam-PDF:iä curlilla.
- IMF: working papers, WEO, Fiscal Monitor, Article IV -raportit (Suomi) – https://www.imf.org/en/Publications
- EKP: working papers, occasional papers, Economic Bulletin
- Euroopan komissio: DG ECFIN (QREA, discussion papers, institutional papers), DG COMP -selvitykset, JRC
- EIB (Investment Report, working papers), BIS working papers, WIPO (aineettomat)

**Akateeminen tutkimus**
- NBER new working papers (erityisesti Productivity, Innovation & Entrepreneurship -ohjelma) – https://www.nber.org/papers
- CEPR discussion papers ja VoxEU, IZA discussion papers, CEP (LSE) discussion/occasional papers
- International Productivity Monitor (https://csls.ca), Economic Policy, AER, QJE, JPE, REStud, Econometrica,
  AEJ-sarjat, Journal of Financial Economics (uudet numerot vain, jos tuottavuusaiheisia)

**Tuottavuuslautakunnat ja tutkimuslaitokset**
- EU:n tuottavuuslautakuntien verkosto ja ProdTool/CompNet (https://www.comp-net.org)
- Kansalliset lautakunnat: Australia Productivity Commission, Ranskan CNP, Irlannin NCPC, Saksan Sachverständigenrat,
  Alankomaiden CPB, Belgia, Portugali, Itävalta, Luxemburg, Uuden-Seelannin Treasury
- Iso-Britannia: The Productivity Institute, ONS (public service productivity), Resolution Foundation
- Bruegel, PIIE, Brookings, McKinsey Global Institute

**Hakusanat** (yhdistä lähteeseen ja kuukauteen): productivity, total factor productivity, business dynamism,
misallocation, market concentration, competition, R&D tax credit, innovation policy, intangible investment,
generative AI productivity, AI adoption firms, public sector productivity, services productivity, management
practices, labour mobility, firm subsidies; suomeksi: tuottavuus, kokonaistuottavuus, luova tuho, kohtaanto,
yritystuet, T&K, aineeton pääoma, tekoäly.

## Rajaus ja pisteytys

Ota mukaan, jos julkaisu käsittelee tuottavuutta tai jotain Tuottavuuslautakunnan teemaa (`raportit.md`,
"Suositusten pysyvä ydin"): palvelut, julkinen sektori, kilpailu ja keskittyminen, yritysdynamiikka ja luova tuho,
T&K- ja innovaatiopolitiikka, aineeton pääoma, osaaminen, tekoäly ja digitalisaatio, yritystuet ja verotus,
työvoiman liikkuvuus, mittaaminen, vihreä siirtymä.

Pisteytä (merkitse ⭐ ne, joita suosittelet):
1. **Suomi-kytkös**: suomalainen aineisto tai Suomi vertailussa → korkein.
2. **TLK-relevanssi**: koskee lautakunnan tuoreinta suositusta tai avointa kysymystä.
3. **Laatu ja painoarvo**: arvostettu julkaisija, vertaisarvioitu tai kausaalinen asetelma, laaja huomio.
4. **Uutuus**: tuo uutta näyttöä verrattuna sivustolla jo oleviin analyyseihin.

Älä ehdota: lehdistötiedotteita ilman taustajulkaisua, mielipidekirjoituksia, pelkkiä tilastojulkistuksia
(paitsi merkittävät, kuten Tilastokeskuksen vuotuiset tuottavuusmittarit), julkaisuja ilman varmistettua linkkiä.

## Ehdotustiedoston muoto

```markdown
# Tutka-ehdotukset VVVV-KK-PP

Aikaikkuna: VVVV-KK-PP – VVVV-KK-PP. Läpikäydyt lähteet: (lyhyt luettelo). Löytyi N uutta.

| # | Julkaisu | Julkaisija, pvm | Miksi kiinnostava |
|---|---|---|---|
| 1 ⭐ | [Tekijät: Nimi](URL) | Julkaisija, sarja nro, pvm | 1–2 virkettä: tulos ja kytkös Suomeen/TLK:hon |

**Huomioita:** esim. lähteet, joita ei saatu auki, ja jonosta päivittyneet julkaisut.
```

Numeroi ehdotukset juoksevasti tiedoston sisällä; käyttäjä vastaa muodossa "1, 3, 5".

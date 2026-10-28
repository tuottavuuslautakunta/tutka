# Tutka – tuottavuustutkimuksen seuranta

GitHub Pages -sivusto, jolla seurataan tuottavuustutkimusta Tuottavuuslautakunnan näkökulmasta.

Sivusto: <https://tuottavuuslautakunta.github.io/tutka/>

## Sisältö

| Polku | Mitä |
|-------|------|
| `index.md` | Etusivu |
| `raportit.md` | Yhteenveto Tuottavuuslautakunnan raporteista 2014–2026 linkkeineen ja läpileikkaavine teemoineen |
| `_tutkimukset/` | Tutkimusyhteenvedot, yksi Markdown-tiedosto per tutkimus |
| `tutkimukset.md` | Tutkimusyhteenvetojen listaus |
| `menetelma.md` | Analyysirakenteen kuvaus lukijoille |
| `.claude/skills/tutkimusanalyysi/` | Claude Code -skill, joka määrittää miten uuden tutkimuksen analyysi tehdään |

## Uuden tutkimuksen lisääminen

Avaa repositorio Claude Codessa ja pyydä esimerkiksi:

> Analysoi tämä tutkimus Tutkaan: https://…

Claude käyttää `tutkimusanalyysi`-skilliä ja kirjoittaa uuden tiedoston `_tutkimukset/`-kansioon. Käsin lisättäessä
kopioi rakenne skillistä tai olemassa olevasta yhteenvedosta.

## Paikallinen esikatselu

```bash
bundle install
bundle exec jekyll serve
```

## Julkaisu

Settings → Pages → *Deploy from a branch* → `main` / `(root)`. GitHub Pages kääntää Jekyll-sivuston automaattisesti.

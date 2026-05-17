# Měření délek

Malá statická aplikace v prohlížeči: měření objektů přes přetažitelné pravítko na plátně, rozhraní s návodovým schématem a rozlišením správně/špatně vyplněných polí.

## Spuštění

### Z GitHubu (GitHub Pages)

Živá verze v prohlížeči (po zapnutí Pages v **Settings → Pages**: zdroj větev `main`, složka `/ (root)`).

**[Spustit aplikaci →](https://frantisekvvb.github.io/mereni_delka/)**

Repozitář: [github.com/FrantisekVvb/mereni_delka](https://github.com/FrantisekVvb/mereni_delka).

### Lokálně

- Otevři `index.html` v prohlížeči nebo servíruj kořen adresáře (např. `npx serve .`).

## Fonty (Fenomen Sans)

Soubory v **`fonts/FenomenSans/`** mají název `FenomenSans-{Book,SemiBold,Bold}.otf` a odpovídají OTF z repozitáře [vividbooks/periodickatabulka](https://github.com/vividbooks/periodickatabulka) (`font/` v hlavní větvi — přímé odkazy jsou v komentáři u `@font-face` v `index.html`). Po klonování je složka prázdná kromě `.gitkeep`; fonty staženy ručně nebo podle té URL. Bez stažených OTF použije CSS zálohu (`local()`, případně systémové sans-serif).

Pro veřejné nasazení zvaž licenci k písmu (OTF jsou díky `.gitignore` z Git povětšinu nekomitované).

## Nasazení na GitHub

1. V adresáři projektu: `git init -b main`
2. `git add .` (binární fonty se díky `.gitignore` nezařadí)
3. Commit a `git remote add origin …`, `git push`

Stránku lze nasadit jako **GitHub Pages** z větve `main`, kořenem repozitáře (soubor `index.html` v rootu stačí).

| Soubor / složka   | Role |
|------------------|------|
| `index.html`     | Jedna stránka: rozvržení, styly a skript |
| `ruler.svg` …    | Obrázky objektů a pravítka na plátně |
| `fonts/FenomenSans/` | Lokální OTF Fenomen Sans ze zdroje výše (git ignorováno) |
| `_write_guide.rb` | Pomocný skript pro vývoj (generování SVG návodu) |

## Licence

K vlastnímu kódu si do repozitáře doplň soubor licence (např. MIT). Písmo **Fenomen Sans** používej v souladu s licencí vlastníka fontu; binární soubory písma projekt kvůli `.gitignore` standardně na GitHub nekomituje.

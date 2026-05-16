# Měření délek

Malá statická aplikace v prohlížeči: měření objektů přes přetažitelné pravítko na plátně, rozhraní s návodovým schématem a rozlišením správně/špatně vyplněných polí.

## Spuštění

- Otevři `index.html` v prohlížeči nebo servíruj kořen adresáře (např. `npx serve .`).

## Fonty (Fenomen Sans)

Webfonty nelze do veřejného repozitáře vkládat bez souhlasu licence. Do složky **`fonts/FenomenSans/`** nahraj podle své licence vlastní soubory s očekávanými názvy (`FenomenSans-Book.woff2`, `FenomenSans-SemiBold.woff2`, `FenomenSans-Bold.woff2`). Po klonování repa bude složka z `.gitkeep` prázdná; bez fontů se použije systémová záloha z CSS (`local()` případně systémové sans-serif).

Post-kloonování: zkopíruj WOFF2 z licencovaného balíku (viz komentář u `@font-face` v `index.html`).

## Nasazení na GitHub

1. V adresáři projektu: `git init -b main`
2. `git add .` (fontové WOFF/WOFF2 se díky `.gitignore` nezařadí)
3. Commit a `git remote add origin …`, `git push`

Stránku lze nasadit jako **GitHub Pages** z větve `main`, kořenem repozitáře (soubor `index.html` v rootu stačí).

| Soubor / složka   | Role |
|------------------|------|
| `index.html`     | Jedna stránka: rozvržení, styly a skript |
| `ruler.svg` …    | Obrázky objektů a pravítka na plátně |
| `fonts/FenomenSans/` | Lokální WOFF2 Fenomen Sans (git ignorováno) |
| `_write_guide.rb` | Pomocný skript pro vývoj (generování SVG návodu) |

## Licence

K vlastnímu kódu si do repozitáře doplň soubor licence (např. MIT). Písmo **Fenomen Sans** drž v mezích licenčního ujednání od vydavatele fontu — binární webfont řezy v tomto projektu do veřejného GitHubu nepatří (viz `.gitignore`).

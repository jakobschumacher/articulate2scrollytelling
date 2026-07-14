# Identitätsmanagement in EMIGA – Scrollytelling

Quarto-Scrollytelling-Umwandlung des Articulate-Rise-Kurses
„Identitätsmanagement (für Standardnutzende)" (Original siehe `index.html` /
`runtime-data.js`, `lib/`, `assets/`). Der Inhalt (Texte, Bilder, Struktur)
wurde aus dem Rise-Export extrahiert und in ein Format im Stil von
<https://nrennie.rbind.io/scrollytelling/> überführt: Der Text scrollt in
einer Spalte, während ein Bild in der anderen Spalte fixiert bleibt und sich
je nach Scrollposition ändert. Technisch genutzt wird die
[Closeread](https://closeread.dev)-Quarto-Extension.

Veröffentlicht via GitHub Pages: <https://jakobschumacher.github.io/articulate2scrollytelling/>

## Lokal rendern / Vorschau

```bash
quarto preview
# oder
quarto render
```

Die Closeread-Extension ist bereits unter `_extensions/qmd-lab/closeread/`
im Repo enthalten, ein `quarto add` ist nicht mehr nötig.

## Struktur

- `index.qmd` – Der komplette Scrollytelling-Inhalt in einem `.cr-section`-Block:
  Einführung → Was ist IDM? → WebAuthn/Passkey → Schritt-für-Schritt-Anleitung
  zur Authentifizierung (Ersteinrichtung + Anmeldung) → Konto gesperrt/
  zurücksetzen → Support.
- `images/` – Die für die Erzählung benötigten Screenshots/Icons.
- `files/` – Das herunterladbare Infomaterial-PDF.
- `styles.css` – Kleine Anpassungen (Akzentfarbe `#046cb4`, Footer-Logos).
- `_extensions/qmd-lab/closeread/` – Die vendorte Closeread-Extension.
- `.github/workflows/publish.yml` – Baut und veröffentlicht die Seite bei
  jedem Push auf `main` automatisch über GitHub Pages.

## Original Articulate-Rise-Export

`index.html`, `lib/`, `assets/`, `runtime-data.js` und `content.Rproj` sind
der unveränderte Original-Export aus Articulate Rise und bleiben als
Referenz erhalten.

## Nicht übernommen

Die Navigationshinweise aus Lektion 0 des Rise-Kurses ("Navigationsmenü",
"Suche", "Grafiken vergrößern") beziehen sich auf die Rise-Player-Oberfläche
und wurden nicht übernommen, da sie in der Quarto-Scrollytelling-Ansicht
nicht zutreffen.

# Identitätsmanagement in EMIGA – Scrollytelling

Dies ist eine Quarto-Scrollytelling-Umwandlung des Articulate-Rise-Kurses
„Identitätsmanagement (für Standardnutzende)" (siehe `../index.html` /
`../runtime-data.js` für das Original). Der Inhalt (Texte, Bilder, Struktur)
wurde aus dem Rise-Export extrahiert und in ein Format im Stil von
<https://nrennie.rbind.io/scrollytelling/> überführt, das den
[Closeread](https://closeread.dev)-Quarto-Extension nutzt: Der Text scrollt
in einer Spalte, während ein Bild in der anderen Spalte fixiert bleibt und
sich je nach Scrollposition ändert.

## Setup

Diese Session hatte keinen Netzwerkzugriff, um die Closeread-Extension
herunterzuladen. Vor dem ersten Rendern muss sie einmalig installiert werden:

```bash
cd scrollytelling
quarto add qmd-lab/closeread
```

Das legt den Ordner `_extensions/closeread/` an (wird per Konvention mit ins
Repo committet, damit spätere Renders ohne erneuten Download funktionieren).

## Rendern / Vorschau

```bash
quarto preview index.qmd
# oder
quarto render index.qmd
```

Das Ergebnis ist eine einzelne, eigenständige HTML-Datei (`index.html`,
`embed-resources: true`), die sich z. B. über GitHub Pages oder Netlify
veröffentlichen lässt.

## Struktur

- `index.qmd` – Der komplette Scrollytelling-Inhalt in einem `.cr-section`-Block:
  Einführung → Was ist IDM? → WebAuthn/Passkey → Schritt-für-Schritt-Anleitung
  zur Authentifizierung (Ersteinrichtung + Anmeldung) → Konto gesperrt/
  zurücksetzen → Support.
- `images/` – Die für die Erzählung benötigten Screenshots/Icons, kopiert aus
  `../assets/`.
- `files/` – Das herunterladbare Infomaterial-PDF.
- `styles.css` – Kleine Anpassungen (Akzentfarbe `#046cb4`, Footer-Logos).

## Nicht übernommen

Die Navigationshinweise aus Lektion 0 des Rise-Kurses ("Navigationsmenü",
"Suche", "Grafiken vergrößern") beziehen sich auf die Rise-Player-Oberfläche
und wurden nicht übernommen, da sie in der Quarto-Scrollytelling-Ansicht
nicht zutreffen.

# Bilder für die Webseite

In diesem Ordner liegen das Logo (`logo.svg`) und das Favicon (`favicon.svg`).
Beide sind fertig und müssen nicht ersetzt werden.

Für die Fotos gibt es auf der Webseite noch graue Platzhalterflächen. Sobald ein
Bild vorliegt, legen Sie es hier ab und ersetzen die Platzhalterfläche im
HTML-Code durch ein `img`-Element (siehe unten).

## Gewünschte Fotos

| Dateiname | Wo es erscheint | Format | Motiv |
|---|---|---|---|
| `portrait.jpg` | ueber-mich.html | Hochformat, ca. 900 × 1200 Pixel | Portrait von Heike Wommelsdorf, freundlich, ruhiger Hintergrund |
| `eingang.jpg` | anfahrt.html | Querformat, ca. 1200 × 800 Pixel | Hauseingang Querstraße 2, so wie man ihn von der Straße sieht |
| `praxis.jpg` | anfahrt.html | Querformat, ca. 1200 × 800 Pixel | Behandlungsraum, aufgeräumt, mit Tageslicht |

Optional, falls vorhanden: ein Detailfoto (Hände bei der Arbeit, Pflanze,
Behandlungsliege) für die Startseite.

## Worauf zu achten ist

- **Dateigröße**: Fotos vor dem Hochladen auf höchstens 300 Kilobyte
  verkleinern, sonst lädt die Seite auf dem Handy langsam. Jedes
  Bildbearbeitungsprogramm kann das („Für Web speichern“, Qualität ca. 75 %).
- **Keine Vorher/Nachher-Bilder** und keine Fotos von Patientinnen oder
  Patienten. Das Heilmittelwerbegesetz verbietet solche Darstellungen in der
  Werbung für Heilbehandlungen.
- **Fremde Bilder** nur mit Lizenz verwenden und die geforderte Namensnennung im
  Impressum unter „Bildnachweis“ eintragen.
- **Menschen auf Fotos** brauchen eine Einwilligung, auch Kolleginnen oder
  Familienangehörige.
- **Dateinamen** klein schreiben, ohne Umlaute und ohne Leerzeichen.

## Platzhalter durch ein Foto ersetzen

Im HTML sieht ein Platzhalter so aus:

```html
<figure class="bild portrait">
  <div class="bild-platzhalter">
    Platzhalter<br>Portraitfoto
  </div>
  <figcaption>
    <span class="platzhalter">[BITTE ERGÄNZEN: …]</span>
  </figcaption>
</figure>
```

Daraus wird:

```html
<figure class="bild portrait">
  <img src="img/portrait.jpg" alt="Heike Wommelsdorf in ihrer Praxis" width="900" height="1200">
  <figcaption>Heike Wommelsdorf, Naturheilpraxis für Faszientherapie</figcaption>
</figure>
```

Der `alt`-Text beschreibt kurz, was auf dem Bild zu sehen ist – er wird
vorgelesen, wenn jemand die Seite nicht sehen kann. Ist das Bild rein
dekorativ, genügt `alt=""`. Wird keine Bildunterschrift gewünscht, kann das
`figcaption`-Element ganz entfallen.

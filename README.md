# Naturheilpraxis Heike Wommelsdorf – Webseite

Webseite der Naturheilpraxis für Faszientherapie, Querstraße 2, 25451 Quickborn.

Die Seite besteht aus reinem HTML und CSS. Es gibt **kein Framework, keine
Datenbank, kein JavaScript und keinen Build-Schritt**. Zum Ansehen genügt ein
Doppelklick auf `index.html` – der Browser zeigt die Seite dann genauso an, wie
sie später im Internet aussieht.

## Dateien

```
index.html              Startseite
faszientherapie.html    Was Faszien sind, Wirkweise, Anwendungsgebiete, FAQ
behandlung.html         Ablauf einer Sitzung, Preise, Kostenerstattung
ueber-mich.html         Vita und Qualifikation
termine.html            Sprechzeiten, Terminvereinbarung, Absageregelung
anfahrt.html            Adresse, Wegbeschreibung, Parken, Zugänglichkeit
impressum.html          Pflichtangaben
datenschutz.html        Datenschutzerklärung
css/style.css           Das einzige Stylesheet (Farben, Schrift, Layout, Druck)
img/logo.svg            Logo: Pinselkreis mit Olivenzweig
img/favicon.svg         Symbol für den Browser-Tab
img/PLATZHALTER.md      Welche Fotos noch fehlen und wie man sie einbaut
```

## Texte ändern

Öffnen Sie die gewünschte `.html`-Datei in einem einfachen Texteditor
(Windows: Notepad, besser: Notepad++ oder VS Code). Der sichtbare Text steht
zwischen den spitzen Klammern:

```html
<p>Dieser Satz erscheint auf der Seite.</p>
```

Ändern Sie nur den Text, nicht die Klammern. Danach die Datei speichern und im
Browser mit F5 neu laden.

Umlaute können normal geschrieben werden (ä, ö, ü, ß), solange die Datei als
**UTF-8** gespeichert wird – das tun alle genannten Editoren von sich aus.

### Wenn eine Änderung auf allen Seiten gelten soll

Kopf- und Fußbereich sind in jeder Datei einzeln enthalten. Das ist der Preis
dafür, dass keine Technik im Hintergrund läuft. Ändern Sie zum Beispiel die
Telefonnummer, müssen Sie sie in allen acht Dateien ersetzen. Am schnellsten geht
das mit „Suchen und Ersetzen in Dateien“ (in VS Code: `Strg+Umschalt+H`).

## Offene Stellen – Inhalte ergänzen

Alle Stellen, an denen noch echte Angaben fehlen, sind im Text gelb markiert und
mit `[BITTE ERGÄNZEN: …]` gekennzeichnet – **derzeit 52 Stellen**. Sie fallen
absichtlich auf, damit keine vergessen wird. Suchen Sie im Editor nach
`BITTE ERGÄNZEN`, um sie alle zu finden.

Zusammengefasst fehlen noch:

| Seite | Was fehlt |
|---|---|
| `termine.html` | Sprechzeiten je Wochentag, Rückrufzeit, Absagefrist und Ausfallhonorar, ggf. Urlaubszeiten |
| `behandlung.html` | Dauer und Preis je Behandlung, akzeptierte Zahlungsmittel |
| `ueber-mich.html` | Werdegang, Ausbildungen mit Jahreszahlen, Heilpraktikererlaubnis, Fortbildungen, Portraitfoto |
| `anfahrt.html` | Wegbeschreibung, Parksituation, AKN-/Bushaltestelle, Etage, Stufen, Barrierefreiheit, Fotos |
| `impressum.html` | Berufsbezeichnung, erteilende Behörde und Aufsichtsbehörde, Berufshaftpflicht, Bildnachweis |
| `datenschutz.html` | Name und Anschrift des Hosters, Speicherdauer der Logdateien, Stand der Erklärung |

Wenn eine Angabe nicht zutrifft, kann die betreffende Zeile ersatzlos gelöscht
werden – zu jedem Platzhalter steht ein Hinweis, was gemeint ist.

## Rechtliches

- **Impressum und Datenschutzerklärung sind Entwürfe, keine Rechtsberatung.**
  Bitte vor dem Livegang gegenlesen lassen, zum Beispiel vom Berufsverband. In
  beiden Dateien steht dazu oben ein grauer Kasten, der anschließend gelöscht
  werden kann.
- **Heilmittelwerbegesetz (HWG):** Die Texte sind bewusst vorsichtig formuliert –
  keine Heilversprechen, keine Erfolgsgarantien, keine Patientenstimmen, keine
  Vorher/Nachher-Bilder. Bitte diesen Ton beibehalten, wenn Sie Texte ergänzen.
  Formulieren Sie „Ziel der Behandlung ist …“ oder „kann unterstützend eingesetzt
  werden“ statt „hilft gegen …“ oder „heilt“.
- **Kein Cookie-Banner nötig:** Die Seite setzt keine Cookies, lädt keine Schriften
  von fremden Servern, bindet keine Karte ein und verwendet keine Analysewerkzeuge.
  Genau deshalb ist kein Einwilligungsbanner erforderlich. Wenn später ein
  Kontaktformular, eine eingebettete Karte oder ein Buchungstool dazukommt, ändert
  sich das – dann muss die Datenschutzerklärung angepasst werden.

## Farben und Schrift

Alle Farben stehen als Variablen am Anfang von `css/style.css` und sind aus der
Visitenkarte abgeleitet:

| Variable | Farbe | Verwendung |
|---|---|---|
| `--creme` | `#F4F1E8` | Seitenhintergrund |
| `--creme-hell` | `#FBF9F4` | Karten, Kopfbereich |
| `--salbei` | `#A9B79E` | Farbflächen, Fußbereich, Schaltflächen |
| `--salbei-hell` | `#C9D2C0` | Linien und dezente Flächen |
| `--olive-dunkel` | `#454F3C` | Fließtext auf Creme |
| `--olive-tief` | `#38402F` | Text auf Salbeiflächen |
| `--olive` | `#6E7F60` | nur große Überschriften und Zierelemente |

Wird eine Farbe dort geändert, ändert sie sich auf allen Seiten.

Die Seite nutzt die Systemschrift des jeweiligen Geräts – dadurch wird nichts von
fremden Servern geladen. Der Charakter der Visitenkarte entsteht über
Großbuchstaben und weite Buchstabenabstände in den Überschriften.

**Google Fonts bitte nicht per Link einbinden** – das überträgt bei jedem
Seitenaufruf die IP-Adresse der Besucher in die USA und ist genau der Grund, warum
diese Seite sonst ein Einwilligungsbanner bräuchte. Wer die Schrift der
Visitenkarte (eine leichte geometrische Schrift wie Jost oder Montserrat Light)
übernehmen möchte, lädt die Datei stattdessen einmal herunter, legt sie als
`css/jost.woff2` ab und ergänzt in `style.css`:

```css
@font-face {
  font-family: "Jost";
  src: url("jost.woff2") format("woff2");
  font-weight: 300 500;
  font-display: swap;
}

:root { --schrift: "Jost", ui-sans-serif, "Segoe UI", Roboto, sans-serif; }
```

## Veröffentlichen

Es müssen einfach alle Dateien und Ordner in dieser Form auf den Webserver – alle
Verweise im Code sind relativ, es ist nichts zu konfigurieren.

**Klassisches Webhosting (Strato, IONOS, All-Inkl. o. ä.):** Mit einem
FTP-Programm wie [FileZilla](https://filezilla-project.org/) verbinden und den
kompletten Inhalt dieses Ordners in das Web-Verzeichnis des Anbieters kopieren
(meist `httpdocs`, `htdocs` oder `public_html`). Die Ordner `css` und `img` müssen
mitkopiert werden. Beim Anbieter „HTTPS erzwingen“ bzw. „SSL-Zertifikat aktivieren“
einschalten.

**Netlify:** Auf [app.netlify.com](https://app.netlify.com/) einloggen und diesen
Ordner in das Feld „Deploy manually“ ziehen – fertig. Alternativ das
Git-Repository verbinden; dann genügt künftig ein `git push`. Build-Befehl bleibt
leer, das Publish-Verzeichnis ist `.`.

**GitHub Pages:** Im Repository unter *Settings → Pages* als Quelle den Branch
`main` und den Ordner `/ (root)` auswählen.

Nach dem Livegang zusätzlich:

- die eigene Domain (`nhp-wommelsdorf.de`) beim Anbieter mit der Seite verbinden,
- die Adresse im Google-Unternehmensprofil hinterlegen, damit die Praxis in der
  Kartensuche gefunden wird,
- zwei Seiten testweise durch <https://validator.w3.org/> prüfen.

## Prüfliste vor dem Livegang

- [ ] Alle 52 `BITTE ERGÄNZEN`-Stellen bearbeitet oder gelöscht
- [ ] Impressum und Datenschutzerklärung gegengelesen, graue Hinweiskästen entfernt
- [ ] Fotos eingesetzt (siehe `img/PLATZHALTER.md`) oder Platzhalter gelöscht
- [ ] Telefonnummer und E-Mail-Adresse auf allen Seiten korrekt
- [ ] Jahreszahl im Fußbereich (`© 2026`) aktuell
- [ ] Auf dem Handy angesehen: nichts ragt seitlich heraus, Telefonnummer antippbar
- [ ] Alle Menüpunkte und die Links im Fußbereich einmal angeklickt

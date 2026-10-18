# Bodyline

Persönliches Körper-Dashboard für Withings-Berichte. Läuft komplett im Browser, ohne Server und ohne Claude.

## Was es kann

- Withings-Gesundheitsbericht (PDF) hochladen: Werte werden automatisch ausgelesen und vor dem Speichern angezeigt
- Figur mit Körperzusammensetzung (Fett, Muskeln, Knochen, Rest)
- Gewichtsverlauf mit Zeitraumwahl, Trends für Fett, Muskeln, Wasser und Grundumsatz
- Kennzahlen: BMI, FFMI, Körperwasser, Tagesbedarf, Eiweiß, Stoffwechselalter, Schritte
- Archiv mit allen Berichten, Original-PDF direkt ansehbar
- Erinnerung an die festen Termine Dienstag und Freitag

## Auf GitHub Pages veröffentlichen

1. Auf github.com ein neues Repository anlegen, z. B. `bodyline`
2. Alle Dateien aus diesem Ordner hochladen („Add file“ → „Upload files“)
3. Im Repository: **Settings → Pages → Branch: `main`, Ordner `/ (root)` → Save**
4. Nach etwa einer Minute ist die App erreichbar unter `https://<dein-name>.github.io/bodyline/`

## Aufs iPhone holen

Seite in Safari öffnen → Teilen → **Zum Home-Bildschirm**. Bodyline startet dann wie eine App, ohne Browserleiste.

## Wo die Daten liegen

Berichte und PDFs werden nur im Browser des jeweiligen Geräts gespeichert (IndexedDB). Im Repository selbst liegen keine Gesundheitsdaten, auch wenn es öffentlich ist.

- Zwischen iPhone und Mac wird nichts automatisch abgeglichen.
- Mit „Sicherung exportieren“ im Archiv eine JSON-Datei speichern, mit „Sicherung importieren“ auf einem anderen Gerät oder nach dem Löschen der Browserdaten wiederherstellen.
- Tipp: Die Sicherung regelmäßig in iCloud Drive ablegen.

## Anpassen

- Körpergröße: in `index.html` die Zeile `const HEIGHT_CM=166` ändern
- Berichtstage: Funktion `cadence()` – `[2,5]` steht für Dienstag und Freitag (0 = Sonntag)

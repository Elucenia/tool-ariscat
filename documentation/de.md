<!-- ELUCENIA technical documentation · ariscat · de · no clinical/professional/rights approval -->

# ARISCAT

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/ariscat)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Alter

`idade`

- `0` — ≤ 50 Jahre
- `3` — 51 bis 80 Jahre
- `16` — \> 80 Jahre

### Präoperative Sauerstoffsättigung (Raumluft, in Ruhe)

`sat`

- `0` — ≥ 96%
- `8` — 91 bis 95%
- `24` — ≤ 90%

### Atemwegsinfektion im letzten Monat

`infec`

### Präoperative Anämie (Hb ≤ 10 g/dL)

`anemia`

### Lokalisation der Inzision

`incisao`

- `0` — Peripher
- `15` — Oberbauch
- `24` — Intrathorakal

### Operationsdauer

`duracao`

- `0` — ≤ 2 h
- `16` — \> 2 h und ≤ 3 h
- `23` — \> 3 h

### Notfalloperation

`emerg`

## Fassung der Methode

ARISCAT/Canet 2010, Tabelle 6: 7 gewichtete Faktoren; Dauer ≤ 2 h = 0, \> 2 h und ≤ 3 h = 16, \> 3 h = 23

## Dokumentierte Formel

Alter 51–80 = 3, \> 80 = 16 · SpO₂ 91–95% = 8, ≤ 90% = 24 · Atemwegsinfektion im letzten Monat = 17 · Hb ≤ 10 g/dL = 11 · Oberbauchinzision = 15, intrathorakale Inzision = 24 · Dauer ≤ 2 h = 0, \> 2 h und ≤ 3 h = 16, \> 3 h = 23 · Notfalloperation = 8.

## Grenzen und Population

ARISCAT 2010 wurde in einer Kohorte von 2464 chirurgischen Patienten aus 59 Krankenhäusern unter Allgemein-, neuraxialer oder Regionalanästhesie entwickelt und validiert; Endpunkt waren postoperative pulmonale Komplikationen. Mindestalter, Ausschlüsse und vollständige Gewichtungen und Bereiche sind im gelesenen Abstract nicht enthalten; die Kohortenraten sind keine für eine andere Population neu kalibrierte individuelle Schätzung. Bei der erneuten Lektüre des Originalartikels von 2010 beschreiben die Methoden Erwachsene ab 18 Jahren und kohortenspezifische Ausschlüsse; Tabelle 6 bestätigt die Dauer ≤2 h, \>2 bis ≤3 h und \>3 h. Die Grenze für hohes Risiko lautet in Tabelle 7 ≥45 und im Text \>45; dieser Widerspruch zwischen den Quellenstellen wurde hier nicht geklärt.

## Referenzen

- [Canet J et al. Prediction of postoperative pulmonary complications in a population-based surgical cohort. Anesthesiology, 2010.](https://doi.org/10.1097/ALN.0b013e3181fc6e0a)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026

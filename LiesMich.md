# AcroScript: Verstecke Hinweis falls Acrobat der Viewer benutzt wird

Ein JavaScript auf Dokument Ebene, welches ein Feld mit einem Hinweis ausblendet, wenn das Dokument in Acrobat oder dem Adobe Reader geöffnet wird.

## Anleitung

1. Öffne die “JavaScript” Werkzeuge in Acrobat
2. Öffne “JavaScript-Anweisungen für Dokumente”
3. Gib einen Namen für das Skript ein und drücke den Button „Hinzufügen“
4. Füge folgenden Code hinzu:
```js
if (app.viewerType == "Exchange" || app.viewerType == "Exchange-Pro" || app.viewerType == "Reader" ) {
    this.getField("NoteAcrobat").display = display.hidden;
}
```
5. Füge ein Formularfeld mit dem Namen „NoteAcrobat“ hinzu

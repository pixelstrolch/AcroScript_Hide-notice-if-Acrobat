# AcroScript: Hide notice if the viewer is Acrobat

Document level script hides field with notice if the PDF document was opened in Acrobat or Adobe Reader.

## How to use

1. Open the “JavaScript” tool
2. Open “Document JavaScripts”
3. Type a script name and push the button “Add”
4. Add the following code:
```js
if (app.viewerType == "Exchange" || app.viewerType == "Exchange-Pro" || app.viewerType == "Reader" ) {
    this.getField("NoteAcrobat").display = display.hidden;
}
```
5. Add a form field and name it “NoteAcrobat”

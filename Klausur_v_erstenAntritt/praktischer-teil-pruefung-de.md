# Prüfung Web-Grundlagen

Laden Sie bitte die Zip-Datei von Moodle herunter und entpacken Sie sie. In der Zip-Datei finden Sie die HTML-Dateien, CSS-Dateien, Bilder und einen Screenshot. Für diese Prüfung werfen Sie bitte einen Blick auf den Screenshot. Ihre endgültige Website sollte wie die Website auf dem Screenshot aussehen. Die folgenden Anweisungen sollen Ihnen helfen, systematisch zum Endergebnis zu gelangen.

**Beachten Sie bitte**: Sie können HTML-Elemente und Attribute hinzufügen, jedoch keine bereits vorhandenen HTML-Elemente neu anordnen oder löschen (ausnahme CSS-Grid container), Text löschen oder Text auskommentieren oder Text hinzufügen. CSS sollte nur zur gegebenen CSS-Datei hinzugefügt werden. Verwenden Sie bitte kein JavaScript um die Elemente zu positionieren oder CSS-Stile anzupassen.

**Upload:**

Nehmen Sie bitte den Ordner und erstellen Sie eine Zip-Datei und laden Sie diese in Moodle hoch.

**Name der Zip-Datei:**
WEB-Nachname-Vorname.zip

## Semantische Elemente

1. Öffnen Sie `index.html` und werfen Sie einen Blick auf alle div-Elemente und ersetzen Sie sie gegebenenfalls durch Blockelemente, die eine semantische Bedeutung haben, z. B.

```html
<!-- Vorher -->
<div id="header"></div>
<!-- Nachher -->
<header id="header"></header>
```

## Navigation

1. Öffnen Sie bitte `index.html` und werfen Sie einen Blick auf den Abschnitt mit der Liste der Links:

```html
<ul>
  <li><a href="\">Home</a></li>
  <li><a href="">Pictures</a></li>
</ul>
```

2. Erstellen Sie einen Link für `Pictures`, der zur HTML-Datei `cats.html` verweist, die sich im Ordner `content` befindet.

## CSS

1. Öffnen Sie `index.html` und erstellen Sie ein Link-Element im Header, der externe CSS-Datei `styles.css` einbindet.

2. Öffnen Sie `cats.html` und erstellen Sie ein Link-Element im Header zur externen Styles-Datei styles.css.

3. Öffnen Sie `styles.css` und wenden Sie folgende CSS-Eigenschaften an:

Überschriftselemente, Absätze, Zitate:

- Benötigte Farben:
  - grey (Überschrift 3 und Absatz)
  - lightslategray (Überschrift 2)
  - darkslategrey (Überschrift 1)
  - darkgrey (Zitat)
- Schriftart (bitte nur auf Überschriftselemente, Absätze und Zitate anwenden):
  - Helvetica
  - sans-serif

4. Wenden Sie die Stile für den Header an.
   - (Tipps: `background: aquamarine`, [Denken Sie an CSS-Box-bezogene Stile und `border` von 2px auf dem unteren Rand des Elements]).
5. Wenden Sie Stile für die Navigation an.
   - (Tipps: `background: grey`, Listenelemente Farbe: `white`,Schriftgröße: `20px`,
   Listenelement Stil: `none`)
6. Listenelemente sollten beim Hover die Farbe `aquamarine` bekommen.
7. Wenden Sie Stile für den Footer an.
   - (Tipps: `background: cornflowerblue`, der Text sollte zentriert sein, [Denken Sie an CSS-Box-bezogene Stile - `padding` von `1rem` wurde nur auf den oberen und unteren Teil vom Element angewendet])
8. Wenden Sie Stile für Kommentare an.
   - (Tipps: `background: aliceblue`, [Denken Sie an CSS-Box-bezogene Stile (`border` - `2px`, `padding` - `.25rem`)])
9. Wenden Sie Stile für Boxen.
   - (Tipps: `background: lightgrey;`, [Denken Sie an CSS-Box-bezogene Stile (`padding` - nur auf der linken und rechten Seite des Elements von `1rem`)])

<div class="page"/>

## Positionierung

1. Die Navigation und der Hauptinhalt sollten in einer Reihe angezeigt werden. Verwenden Sie Flexbox oder CSS-Grid, um dies zu erreichen.

2. Die Artikel und Kommentare sollten übereinander angeordnet sein. Verwenden Sie Flexbox oder CSS-Grid, um dies zu erreichen.

3. Die drei Boxen sollten in einer Reihe sein, wenn genügend Platz vorhanden ist. Wenn nicht genügend Platz vorhanden ist, sollten sie eine neue Reihe beginnen. Verwenden Sie bitte ausschließlich Flexbox, um dies zu erreichen.
   - Tipp: Abstand (Gap) zwischen Boxelementen beträgt `1rem`

4. Innerhalb einer Box sollten die Inhalte in einer Spalte angeordnet sein. Zentrieren Sie das Bild (Tipp: Verwenden Sie die `align-self` Eigenschaft im CSS Elementselektor für das Bild). Verwenden Sie bitte ausschließlich Flexbox, um dies zu erreichen.

## Javascript

Werfen Sie einen Blick auf den folgenden Abschnitt:

```html
<section id="cookieblock">By using this website, you automatically accept that we use cookies.<button>Understood</button></section>
```

1. Wenn auf den Button "Understood" geklickt wird, sollte ein Cookie mit dem Namen "CookieBlock" auf "Understood" gesetzt werden. Das Cookie sollte nach 3 Monaten ablaufen.
   - (Tipp: Sie können das `onclick`-Attribut des Button-Elements verwenden)
   - (Tipp: Wie man Cookies setzt, kann hier angeschaut werden: https://www.w3schools.com/js/js_cookies.asp)

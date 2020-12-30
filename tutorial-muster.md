# Ein Muster für Anleitungen
--Das alles kann man gut gebrauchen
--### @explicitHints true 
--### @flyoutOnly true für Expand aller Blöcke in der Toolbox
--### @hideIteration true verbirgt Schritte
--### @diffs true zeigt Diffs zwischen Steps

Dieser Code ist Basis des Programmes, nicht in der Anleitung:

```template
let x = 0
basic.showString("Hello!")
basic.clearScreen()
```

## ~avatar avatar @unplugged

**So schliesst Du Deinen @boardname@ am Laptop an.**

Bild einbetten:

![Am Computer anschliessen](https://github.com/CalliTGS3/calliope-tutorial/blob/master/Am_Computer_anschliessen_2.jpg?raw=true)

## Ein wenig Markdown @unplugged

Text der Anleitung <br>
**Text fett** <br>
*Text kursiv*

- ungeordneter Punkt 1
- ungeordneter Punkt 2
- ungeordneter Punkt 3

1. geordneter Punkt 1
2. geordneter Punkt 2
3. geordneter Punkt 3

Eine Tabelle:

| Linke Überschrift | Rechte Überschrift |
| ------------------ | ------------------ |
| Etwas Text hier | Ein bisschen hier |

Eine Tabelle mit Textausrichtung:

| Überschrift 1 | Überschrift 2 | Überschrift 3 |
|:--------------|:-------------:|--------------:|
| Links | Zentriert | Rechts |


## Schritt 1 @fullscreen

Erstelle eine Variable ``||Variables:x||`` und setze diese auf den Wert 10.
Setze diese Zuweisung in den Block  ``||Basic:beim Start||``.
Setze Deine Variable so: ``[let x = 5]``


## Schritt 2 

Block anzeigen:

```blocks
let y = 10
```

#### ~hint

##### Hinweis Schritt 2
Das ist ein Hinweis für Schritt 2


## Schritt 3 

Block mit Signatur der Funktion:

```sig
basic.showNumber(5)
```


## Schritt 4

Code Karten anzeigen:

```cards
basic.showNumber(0)
basic.showLeds(`
. . . . .
. . . . .
. . # . .
. . . . .
. . . . .
`)
basic.showString("Hello!")
basic.clearScreen()
```

## Schritt 5

Namespaces anzeigen:

```namespaces
basic.showNumber(0)
input.onButtonPressed(() => {})
```

## Schritt 6

```typescript
let x = 0
```


## Schritt 7

Damit der Block in der Auswahl erscheint:

```ghost
basic.pause(100)
```


## Schritt 8

Alle Blöcke eines Namespaces:

```apis
basic
```

## Schritt 9

Pseudocode schreibt man so:

```typescript-ignore
// You can include illegal TS in here, e.g. to showcase concepts/psuedocode
for (initialization; check; update) {
    ...
}
```


## Schritt 10

Ungültiger Code:

```typescript-invalid
// You can include illegal TS in here, e.g. to document syntax errors
callFunction(;
```


## Schritt 11

Gültiger Code:

```typescript-valid
// You can include any TS in here, e.g. to showcase correct syntax
callFunction()
```


## Schritt 12

highlight Code:

```blocks
console.log(":)")
// @highlight
console.log(":(")
```


## ~ @unplugged
Ende.
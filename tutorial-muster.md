# Ein Muster für Anleitungen
### @ explicitHints true 
### @ flyoutOnly true für Expand aller Blöcke in der Toolbox
### @ hideIteration true verbirgt Schritte
### @diffs true zeigt Diffs zwischen Steps

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

Text der Anleitung mit erzwungenem Zeilenumbruch <br>
**Text fett** <br>
*Text kursiv*

Liste:
- ungeordneter Punkt 1
- ungeordneter Punkt 2
- ungeordneter Punkt 3

Geordnete Liste:
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


## Blöcke und Farben aus der Toolbox @fullscreen

Erstelle eine Variable ``||Variables:x||`` und setze diese auf den Wert 10.
Setze diese Zuweisung in den Block  ``||Basic:beim Start||``.
Setze Deine Variable so: ``[let x = 5]``


## Blöcke @fullscreen

Block anzeigen:

```blocks
let y = 10
```


## Beispiel Blinkendes Herz Schritt 1 @fullscreen

Nimm den Block ``||basic:zeige LEDs||`` und setze ihn in den ``||basic:dauerhaft||`` Block.
Zeichne ein Herz mit der Maus, indem Du einzeln auf die LED Symbole drückst.

Den ``||basic:beim Start||`` Block brauchen wir in diesem Programm nicht. Den Block kannst Du löschen, indem Du mit der rechten Maustaste auf ihn zeigst und "Block löschen" auswählst.

```blocks
basic.forever(function() {
    basic.showLeds(`
        . # . # .
        # # # # #
        # # # # #
        . # # # .
        . . # . .`);
})
```


## Beispiel Blinkendes Herz Schritt 2 @fullscreen

Nimm noch einen ``|| basic:zeige LEDs ||`` Block und ordne ihn direkt unterhalb des ersten im Programm an. Du kannst ihn leer lassen oder ein kleineres Herz zeichnen.

```blocks
basic.forever(function() {
    basic.showLeds(`
        . # . # .
        # # # # #
        # # # # #
        . # # # .
        . . # . .`);
    basic.showLeds(`
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        . . . . .`);
})
```


## ~ @unplugged
Ende.
# Blinkendes Herz

## Willkommen @unplugged
In diesem Tutorial lernst du, wie Du mit Deinem @boardname@ ein blinkendes Herz programmierst!
Hinweis: Machmal musst du scrollen um den "Weiter" Button zu sehen!


## Schritt 1 @showhint

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


## Schritt 2 @showhint

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

## Schritt 3

Schau Dir im @boardname@ Simulator Dein Programm an, Du solltest ein blinkendes Herz sehen.


## Schritt 4 @showhint

Wenn Du es langsamer blinken lassen willst, kannst Du einen ``||basic:pausiere (ms)||`` Block mit 1 Sekunde hinzufügen:
Achte darauf, an welcher Stelle die Anzeige die Pause macht. Du kannst auch eine zweite Pause hinter dem zweitem ``|| basic:zeige LEDs ||`` Block einfügen.

```blocks
basic.forever(function() {
    basic.showLeds(`
        . # . # .
        # # # # #
        # # # # #
        . # # # .
        . . # . .`);
    basic.pause(1000)
    basic.showLeds(`
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        . . . . .`);
})
```


## Schritt 5 @showhint

Schliesse Deinen @boardname@ mit dem USB Kabel an und drücke auf ``|Herunterladen|``. 
Damit wird Dein Programm zum @boardname@ übertragen.


## Schritt 6

Gut gemacht! Du hast ein MakeCode geschrieben, welches deinen @boardname@ ein blinkendes Hez anzeigen lässt!
Verlasse diese Anleitung, indem Du auf ``|Fertig|`` klickst. Durch klicken auf ``|Beenden|`` kannst du ein anderes Tutorial wählen!

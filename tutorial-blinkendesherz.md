# Blinkendes Herz

## Schritt 1 @showhint

Nimm den Block ``||basic:zeige LEDs||`` und setze ihn in den ``||basic:dauerhaft||`` Block.
Zeichne ein Herz mit der Maus, indem Du einzeln auf die LED Symbole drückst.

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
Den ``||basic:beim Start||`` Block brauchen wir in diesem Programm nicht. Den Block kannst Du löschen, indem Du mit der rechten Maustaste auf ihn zeigst und "Block löschen" auswählst.


## Schritt 2

Nimm noch einen Block ``||basic:zeige Leds||`` block. Du kannst ihn leer lassen oder ein kleineres Herz zeichnen.

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

## Schritt 4

Schliesse Deinen @boardname@ mit einem USB Kable an und drücke auf ``|Herunterladen|``. Speichere Dein Programm auf dem Laufwerk **@drivename@**. 
Damit wird Dein Programm zum @boardname@ übertragen.

## Schritt 5

Gut gemacht! Du hast Dein erstes MakeCode Programm für den @boardname@ geschrieben.

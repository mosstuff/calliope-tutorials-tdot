# Die 5x5 LED Matrix

## ~avatar avatar @unplugged

Der @boardname@ hat 25 rote LEDs, die einzeln ein- und ausgeschaltet werden können. 
Du kannst auch fertige Symbole, Text und Zahlen darstellen und musst Dir keine Gedanken machen, 
welche LED's Du ein - oder ausschalten musst.


## Schritt 1 @fullscreen

**Anzeige eines Textes**

Um einen Text (auch Zeichenkette genannt) mit der LED-Matrix anzuzeigen, wähle im Menü Basis den Block ``||Basic:zeige Text||`` aus,
gib den von Dir gewünschten Text ein und setze diesen Block in das Hauptprogramm. 

```blocks
basic.showString("hi!")
```

Du kannst auch den Inhalt von 
Text - Variablen anzeigen:

```blocks
let meinText = "Hi!"
basic.showString(meinText)
```


## Schritt 2 @fullscreen

**Anzeige einer Zahl**

Um eine Zahl mit der LED-Matrix anzuzeigen, wähle im Menü Basis den Block ``||Basic:zeige Zahl||`` aus,
gib den von Dir gewünschte Zahl ein und setze diesen Block in das Hauptprogramm. 

```blocks
basic.showNumber(5)
```

Du kannst auch den Inhalt von 
Zahlen - Variablen anzeigen:

```blocks
let meineZahl = 10
basic.showString(meineZahl)
```


## Schritt 3 @fullscreen

**Anzeige eines Symbols**

Um ein Symbol, zB. ein Herz oder ein Kreuz mit der LED-Matrix anzuzeigen, wähle im Menü Basis den Block ``||Basic:zeige Symbol||`` aus,
wähle das von Dir gewünschte Symbol aus und setze diesen Block in das Hauptprogramm. 

```blocks
basic.showIcon(IconNames.Heart)
```

Du kannst auch eigene Symbole erstellen: 
Wähle einfach den Block ``||Basic:zeige LEDs||`` 
aus dem Menü Basis und klicke in beliebige Felder, 
um Dein eigenes Bild zu erstellen.

```blocks
basic.showLeds(`
    . . . . .
    . . . . .
    . . . . .
    . . . . .
    . . . . .
    `)
```

# Klickzähler

## ~avatar avatar @unplugged

Um einfach Dinge oder Personen zu zählen, verwendet man oft sogenannte Handzähler oder Klickzähler.
Man kann solche Handzähler zum Beispiel benutzen, um die Personen in einem Raum zu zählen, auch wenn ständig jemand hineingeht oder herauskommt.


## Schritt 1 @fullscreen

Auf dem 5x5 Display des Calliope mini wollen wir die gezählten Dinge oder Personen anzeigen.
Wir nehmen aus dem Bereich ``||basic:Grundlagen ||`` den Block ``||basic: zeige Zahl||``. <br>
Dieser wird in den Block ``||basic:dauerhaft||`` geschoben. Im Simulator wird dir nun die Zahl angezeigt, welche im Block ``||basic: zeige Zahl||`` steht. <br>
Diese Zahl wollen wir mit den Knöpfen A und B des Calliope mini verändern können. 

```blocks
basic.forever(function () {
    basic.showNumber(0)
})
```

## Schritt 2 @fullscreen

Um die angezeigte Zahl mit den Knöpfen A und B am Calliope verändern zu können, dürfen wir sie nicht direkt in den Block ``||basic: zeige Zahl||`` programmieren, sondern müssen sie in einer Variable speichern. <br>
In einer Variable kannst du in einem Computer Zahlen, Buchstaben, Wörter oder Listen aufbewahren. <br>
Man kann zum Beipiel eine Zahl in eine Variable schreiben und sie später wieder auslesen.
Erstelle eine Variable namens ``||Variables:Zähler||``, indem du auf den Bereich ``||Variables:Variablen||`` klickst. <br>


## Schritt 3

Nach dem Erstellen erscheinen nun die Blöcke ``||Variables:setze auf||`` und ``||Variables:ändere um||`` im Bereich ``||Variables:Variablen||``. <br>
Den Block ``||Variables:setze auf ||`` setzt Du in den Programmblock ``||basic:beim Start||``. 
So wird der Variable beim Start des Calliope der Wert 0 zugewiesen. <br>

```blocks
let Zähler = 0
Zähler = 0
```

## Schritt 4

Um uns jetzt die gespeicherte Zahl dauernd anzeigen zu lassen, nehmen wir den Block ``||Variables:Zähler||`` und schieben ihn in den Block ``||basic: zeige Zahl||``. <br>

```blocks
basic.forever(function () {
    basic.showNumber(Zähler)
})
```

## Schritt 5

Die Variable kannst mit einem Knopfdruck auf Taste A erhöhen, indem Du den Block ``||input:wenn Knopf A gedrückt||`` aus dem Bereich ``||input:Eingaben||`` nehmen und uns hier den Block ``||Variables:ändere um 1 ||`` hineinschieben. <br>
Da in dem Block "ändere um 1" steht, erhöht sich die Variable um eins bei jedem Drücken des Knopfes.

```blocks
input.onButtonPressed(Button.A, function () {
    Zähler += 1
})

```


## Schritt 6

Die Variable kannst mit einem Knopfdruck auf Taste B verringen, indem Du den Block ``||input:wenn Knopf B gedrückt||`` aus dem Bereich ``||input:Eingaben||`` nehmen und uns hier den Block ``||Variables:ändere um 1 ||`` hineinschieben. <br>
(Hinweis. Schiebe erst den Block ``||input:wenn Knopf A gedrückt||`` in Dein Programm und ändere dann den Knopf auf ``||input:B||``)
Da in dem Block "ändere um - 1" steht, verringert sich die Variable um eins bei jedem Drücken des Knopfes.

```blocks
input.onButtonPressed(Button.B, function () {
    Zähler += -1
})

```


## Schritt 7

Um den Zähler auch wieder zurücksetzen zu können, kann man beispielsweise die Tasten A und B gleichzeitig drücken, wenn hier in den Block ``||input:wenn Knopf A+B gedrückt||`` 
der Block ``||Variables:setze auf 0 ||`` geschoben wird.
(Hinweis. Schiebe erst den Block ``||input:wenn Knopf A gedrückt||`` in Dein Programm und ändere dann den Knopf auf ``||input:A+B||``)

```blocks
input.onButtonPressed(Button.AB, function () {
    Zähler = 0
})
```


## Schritt 8 @fullscreen
So sollte Dein Programm jetzt aussehen:
```blocks
let Zähler = 0
Zähler = 0
input.onButtonPressed(Button.A, function () {
    Zähler += 1
})
input.onButtonPressed(Button.B, function () {
    Zähler -= 1
})
input.onButtonPressed(Button.AB, function () {
    Zähler = 0
})
basic.forever(function () {
    basic.showNumber(Zähler)
})
```


## Schritt 9

Schau Dir im @boardname@ Simulator Dein Programm an, Du kannst dort auch mit der Maus die beiden Tasten A und B bedienen.


## Schritt 10

Schliesse Deinen @boardname@ mit einem USB Kabel an und drücke auf ``|Herunterladen|``. Speichere Dein Programm auf dem Laufwerk **@drivename@**. 
Damit wird Dein Programm zum @boardname@ übertragen.


## Schritt 11
Nach dem Fertigstellen:
Im Hauptmenü von makecode findest Du den Menüpunkt ``|Teilen|``. 
Klicke darauf, Du siehst anschließend ein Fenster in der Mitte mit dem Namen des Projektes. 
Klicke auf die Schaltfläche ``|Projekt veröffentlichen|`` und dann auf ``|Link|`` kopieren. 
Danach kannst Du diesen Link in der Schulcloud als Lösung zu der Aufgabe eintragen.


## Schritt 12

Gut gemacht! Du hast einen Klickzähler für den @boardname@ geschrieben.
Verlasse diese Anleitung, indem Du auf ``|Fertigstellen|`` klickst. 

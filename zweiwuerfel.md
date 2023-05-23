# Zwei Würfel

## Einleitung @unplugged

Baue ein Würfelspiel für zwei Spieler mit dem @boardname@. Die **Funk** Blöcke erlauben das Austauschen von Nachrichten von einem @boardname@ mit einem anderen @boardname@.

Wir brauchen zwei @boardname@ und auf beide müssen wir das gleiche Programm übertragen.

In diesem Spiel schüttelst Du den Würfel auf dem @boardname@ und sendest die Zahl der Augen zu dem anderen @boardname@. Der andere @boardname@ macht das genauso. Wenn Du eine Zahl von Augen größer oder gleich Deiner Anzahl empfängst, hast Du verloren.

## Würfelspiel @fullscreen

Laß uns beginnen das **Würfel Spiel für Zwei** zu programmieren.

```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showNumber(Math.randomRange(1, 6))
})
```

## Variable Augen @fullscreen

Wir müssen die Anzahl der Augen in einer Variablen speichern. Eine **Variable** ist ein Platz im Speicher des @boardname@ den wir über den Namen der Variablen wiederfinden, und er speichert unsere Daten, zB. eine Zahl.

* Gehe zur Toolbox **Variablen** und klicke ``||Erstelle eine Variable..||`` um eine neue Variable anzulegen. Wir nennen sie **Augen**. 
* Füge einen ``||setze Augen auf||`` Block in das Programm und ``||wähle eine zufällige Zahl von bis ||`` darin aus.
* Füge einen ``||Augen||`` aus der **Variablen** Toolbox in einen ``||Grundlagen:Zeige Zahl||`` Block.

```blocks
let Augen = 0
input.onGesture(Gesture.Shake, function () {
    Augen = Math.randomRange(1, 6)
    basic.showNumber(Augen)
})
```

## Sende die Augen @fullscreen

Plaziere einen ``||Funk:sende Zahl über Funk||`` und ``||Augen||`` in das Programm, um die ``Augen`` Variable über Funk an den anderen @boardname@ zu senden.

```blocks
let Augen = 0
input.onGesture(Gesture.Shake, function () {
    Augen = Math.randomRange(1, 6)
    basic.showNumber(Augen)
    radio.sendNumber(Augen)
})
```

## Empfange die Augen @fullscreen

Plaziere einen ``||Funk:wenn Zahl empfangen||`` Ereignis Block in deinem Programm. Dieser Block wird aufgerufen wenn eine Nachricht von dem anderen @boardname@ eintrifft. Der ``receivedNumber`` Wert  ist die Anzahl der Augen deines Mitspeilers mit dem anderen @boardname@.

```blocks
radio.onReceivedNumber(function (receivedNumber) {
})
```

## Teste wer gewonnen hat @fullscreen

Plaziere einen ``||Logikc:wenn||`` Block in dem Ereignis, um zu überprüfen, ob ``receivedNumber`` größer oder gleich ``Augen`` ist. 
Wenn das der Fall ist, hast Du verloren. Zeige ein weinendes Gesicht an.

Programmiere selbständig, ein lachendes Gesicht anzuzeigen!

```blocks
let Augen = 0;
radio.onReceivedNumber(function (receivedNumber) {
    if (receivedNumber >= Augen) {
        basic.showIcon(IconNames.Sad)
    }
})
```

## Teste dein Programm im Simulator! @fullscreen

Drücke **SCHÜTTELN** im Simulator und schaue was auf dem zweiten @boardname@ passiert. Du kannst das auf beiden virtuellen Boards probieren.

Überspiele das Programm auf beide @boardname@, und spiele das Spiel mit deinem Freund!

```blocks
let Augen = 0
input.onGesture(Gesture.Shake, function () {
    Augen = Math.randomRange(1, 6)
    basic.showNumber(Augen)
    radio.sendNumber(Augen)
})
radio.onReceivedNumber(function (receivedNumber) {
    if (receivedNumber >= Augen) {
        basic.showIcon(IconNames.Sad)
    }
})
```

```package
radio
```

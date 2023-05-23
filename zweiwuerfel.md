# Zwei Würfel

## Einleitung @unplugged

Baue ein Würfelspiel mit dem Calliope mini **Funk**. Die **Funk** Blöcke erlauben das Austauschen von Nachrichten von einem @boardname@ mit einem anderen @boardname@.

In diesem Spiel schüttelst Du den Würfel auf dem @boardname@ und sendet die Zahl der Augen zu dem anderen @boardname@. Wenn Du eine Zahl von Augen größer oder gleich Deiner Anzahl empfängst, hast Du verloren.

## Würfelspiel @fullscreen

Laß uns beginnen das **Würfel** Spiel zu programmieren.

```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showNumber(Math.randomRange(1, 6))
})
```

## Variable Augen @fullscreen

Wir müssen die Anzahl der Augen in einer Variablen speichern. Eine **Variable** ist ein Platz im Speicher des @boardname@ den wier über den Namen der Variablen wiederfinden, und er speichert unsere Daten, zB. eine Zahl.

* Gehe zur Toolbox **Variablen** und klicke ``||Make a Variable||`` um eine neue Variable anzulegen. Wir nenen sie **Augen**. 
* Füge einen ``||setze Augen auf||`` block in das Programm und ``||wähle Zufallszahl ||`` darin aus.
* Füge einen ``||Augen||`` aus dem **Variablen** Toolbox in einen ``||basic:show number||`` Block.

```blocks
let Augen = 0
input.onGesture(Gesture.Shake, function () {
    Augen = Math.randomRange(1, 6)
    basic.showNumber(Augen)
})
```

## Sende die Augen @fullscreen

Plaziere einen ``||radio:send number||`` und ``||Augen||`` in das Programm, um die ``Augen`` Variable über Funk zu senden.

```blocks
let Augen = 0
input.onGesture(Gesture.Shake, function () {
    Augen = Math.randomRange(1, 6)
    basic.showNumber(Augen)
    radio.sendNumber(Augen)
})
```

## Empfange die Augen @fullscreen

Go get an ``||radio:on received number||`` event block. This event runs when a radio message from another @boardname@ arrives. The ``receivedNumber`` value is the value of the dice in this game.

```blocks
radio.onReceivedNumber(function (receivedNumber) {
})
```

## Check your cast @fullscreen

Add a ``||logic:if||`` block to test if ``receivedNumber`` is greater or equal to ``dice``. 
If is, you lost so display a sad face on the screen.

```blocks
let Augen = 0;
radio.onReceivedNumber(function (receivedNumber) {
    if (receivedNumber >= Augen) {
        basic.showIcon(IconNames.Sad)
    }
})
```

## Test it! @fullscreen

Try pressing **SHAKE** in the simulator and see that a second @boardname@ appears. You can play the game on both virtual boards.

If you have more than one @boardname@, download your code onto each one and try playing the game with your friends!

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

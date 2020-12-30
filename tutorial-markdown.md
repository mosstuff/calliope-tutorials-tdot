# Markdown
## Schritt 3 @fullscreen

Block mit Signatur der Funktion:

```sig
basic.showNumber(5)
```


## Schritt 4 @unplugged

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

## Schritt 5 @fullscreen

Namespaces anzeigen:

```namespaces
basic.showNumber(0)
input.onButtonPressed(() => {})
```

## Schritt 6 @fullscreen

```typescript
let x = 0
```


## Schritt 7 @fullscreen

Damit der Block in der Auswahl erscheint:

```ghost
basic.pause(100)
```


## Schritt 8 @fullscreen

Alle Blöcke eines Namespaces:

```apis
basic
```

## Schritt 9 @fullscreen

Pseudocode schreibt man so:

```typescript-ignore
// You can include illegal TS in here, e.g. to showcase concepts/psuedocode
for (initialization; check; update) {
    ...
}
```


## Schritt 10 @fullscreen

Ungültiger Code:

```typescript-invalid
// You can include illegal TS in here, e.g. to document syntax errors
callFunction(;
```


## Schritt 11 @fullscreen

Gültiger Code:

```typescript-valid
// You can include any TS in here, e.g. to showcase correct syntax
callFunction()
```


## Schritt 12 @fullscreen

highlight Code:

```blocks
console.log(":)")
// @highlight
console.log(":(")
```


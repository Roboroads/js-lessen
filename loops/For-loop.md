# For-loop: wanneer je al weet hoe vaak je wil herhalen.

Een for-loop gebruik je vooral als je al weet hoe vaak je wil herhalen. De meeste gebruikelijk vorm van een for-loop heeft te maken met nummers. Een for-loop bestaat uit 3 delen:

 1. We beginnen met [iets]
 2. We loopen zolang [iets] true is (m.a.w.: condition)
 3. Elke loop doen we [iets]

## Voorbeeld

Het simpelste en meest gebruikte is een for-loop waarbij we beginnen met een nummer, en zolang dat nummer niet een bepaald ander nummer bereikt heeft loopen we. In dit geval:

 1. We beginnen met een variabele die bijv. op 10 staat: `var i = 10;`
 2. We loopen zolang als deze variabele groter dan 0 is: `i > 0;`
 3. Elke loop willen we -1 doen op deze variabele: `i = i - 1;` \
 *`i = i - 1;` kan korter geschreven worden, zoals `i -= 1`, maar omdat het 1 is, kan je ook `i--` gebruiken. In het volgende voorbeeld gebruik ik `i--` omdat dat het gebruikelijkst is.*

Of in code:

```js
for(var i = 10; i > 0; i--) {
	console.log(i);
}
```

Geeft deze output:

```txt
10
9
8
7
6
5
4
3
2
1

// Let op: geen 0, want zodra [i = 0], is [i > 0 = false], dus stopt de loop.
```

## Opdracht 1

Schrijf een for-loop, waarbij de uitkomst als volgt is:

```txt
0
1
2
3
4
5
```

## Opdracht 2

Schrijf een for-loop, waarbij de uitkomst als volgt is:

```txt
2
4
6
8
10
```

Extra punt als je **geen** berekeningen doet tussen de `{}` van de for-loop.

## Bonus info

Hoewel in letterlijk elk online voorbeeld de variabele `var i = 1;` wordt gebruikt, de variabele hoeft geen `i` te heten. `for(var horizontal = 10; horizontal < 700; horizontal++)` werkt ook prima.

En hoewel we in elk statement elke keer dezelfde variabele gebruiken, ook dat is niet perse nodig! Ook dit werkt:

```js
var double = 0;
for(var i = 1; double < 400; i++) {
	double = 2 * i;
}
```

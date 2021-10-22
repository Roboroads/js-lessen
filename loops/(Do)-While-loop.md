# While-loop: Wanneer je **voor** elke iteratie gaat kijken of je door wil gaan met loopen

Soms weet je in de loop pas of je door wil gaan of niet. Bijv. wanneer je resultaten ophaalt uit een database maar niet precies weet hoeveel rijen er zijn. Een while-loop heeft maar 1 onderdeel, wat nummer 2 was bij de for-loop: "We loopen zolang <iets> true is".


## Voorbeeld

Ik wil loopen totdat `row = null;`. In dit voorbeeld gebruik ik een functie `getRowFromDatabase` waarvan ik weet dat die een rij teruggeeft als er nog een rij is, en anders `null`. Dat is in code:

```js
var row = getRowFromDatabase();
while(row != null) {
	row = getRowFromDatabase();
}
```

## Let op: conditie is vooraf!

Belangrijk om te weten bij while, is dat als de conditie in de while al waar is voordat de loop begint, er nooit geloopt wordt. 

```js
var row = null;
// omdat [row = null], is deze condition al false, dus wordt de loop niet uitgevoerd.
while(row != null) { 
	row = getRowFromDatabase();
}
```
Als je wil dat de condition NA de loop wordt gecontroleerd, kijk dan hieronder bij Do-While loops.

## Opdracht

Kopieer dit stukje code en schrijf je opdracht er onder.

```
// Deze functie genereerd een nummer tussen 1 en 10 (inclusief 1 en 10)
function randomNumber() {
	var generated = Math.floor(Math.random() * 10) + 1;
	console.log(generated);
	return generated;
}
```

Opdracht: roep randomNumber() aan tot je een 9 of een 10 terugkrijgt.

# Do-While-loop: Wanneer je **na** elke iteratie gaat kijken of je door wil gaan met loopen

Een do-while-loop is gelijk aan een while-loop, echter wordt pas **na** elke iteratie gekeken of de conditie waar is. Handig als je zeker weet dat je in ieder geval 1x de loop wil uitvoeren.

## Voorbeeld

Ik wil loopen totdat `row = null;`. In dit voorbeeld gebruik ik een functie `getRowFromDatabase` waarvan ik weet dat die een rij teruggeeft als er nog een rij is, en anders `null`. Dat is in code:

```js
var row = null;
do {
	row = getRowFromDatabase();
} while(row != null);
```

Zoals je ziet kan ik nu wel `var row = null;` doen - omdat de loop sowieso 1x wordt uitgevoerd, en pas daarna owrdt gekeken of `row != null`.

## Opdracht

Dezelfde als voor while, maar nu wil ik dat je stopt als het getal even is. (Tip: gebruik modulo voor korte code!)
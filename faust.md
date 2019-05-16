# FAUST

## operatori matematici

`+ – * /`

ogni operatore matematico implica la presenza di due segnali, rispettivamente a sinistra e a destra dell'operatore.

le due espressioni `process = +;` e `process = _ + _;` sono equivalenti.

![somma](https://raw.githubusercontent.com/LSSN/appunti/master/code/somma-svg/process.png)

ogni operatore matematico necessita quindi di due entrate e restituisce una sola uscita.

## gestione segnali

`_` (trattino basso, identifica il segnale audio, implicito negli operatori matematici)

`:` (identifica un percorso seriale, ovvero in sequenza)

`,` (identifica un percorso parallelo)

### Percorso seriale:

```
import("stdfaust.lib");
process = *(1.0): *(1.0);
```

![seriale](https://raw.githubusercontent.com/LSSN/appunti/master/code/seriale-svg/process.png)

### Percorso parallelo:

```
import("stdfaust.lib");
process = *(1.0), *(1.0);
```

![parallelo](https://raw.githubusercontent.com/LSSN/appunti/master/code/parallelo-svg/process.png)

### Percorso ibrido:

```
import("stdfaust.lib");
process = +,+:+;
```

![parallelo](https://raw.githubusercontent.com/LSSN/appunti/master/code/ibrido-svg/process.png)

## regole base

un commento si scrive con due `//`

ogni programma deve avere le seguenti righe:

```
import("stdfaust.lib");

process = scrivi qui il tuo programma ;
```
ogni programma può avere una sola riga `process`.

ogni riga termina con un `;`

## diagramma di flusso

un digramma di flusso indica il percorso dei segnali ed i processi ad essi applicati.

![diagramma](https://raw.githubusercontent.com/LSSN/appunti/master/code/diagramma-svg/process.png)

abbiamo due segnali in entrata che vengono sommati tra loro e poi moltiplicati per una costante.

# FAUST

## operatori matematici

Ogni operatore matematico `+ – * /` implica la presenza di due segnali, rispettivamente a sinistra e a destra dell'operatore. Le due espressioni `process = +;` e `process = _+_;` sono quindi equivalenti.

![somma](https://raw.githubusercontent.com/LSSN/appunti/master/code/somma-svg/process.png)

Ogni operatore matematico necessita quindi di due entrate e restituisce una sola uscita.

## gestione segnali

 - `_` trattino basso, identifica il segnale audio, implicito negli operatori matematici
 - `:` identifica un percorso seriale, ovvero in sequenza
 - `,` identifica un percorso parallelo
 - `<:` divide il percorso di segnale in molteplici percorsi paralleli ordinati tra loro
 - `:>` combina molteplici segnali paralleli in un percorso
 - `~` identifica una ricorsione 

### percorso seriale:

```
import("stdfaust.lib");
process = *(1.0): *(1.0);
```

![seriale](https://raw.githubusercontent.com/LSSN/appunti/master/code/seriale-svg/process.png)

Il programma esegue due moltiplicazioni in sequenza tra loro.

### percorso parallelo:

```
import("stdfaust.lib");
process = *(1.0), *(1.0);
```

![parallelo](https://raw.githubusercontent.com/LSSN/appunti/master/code/parallelo-svg/process.png)

Il programma esegue due moltiplicazioni contemporanee ed indipendenti tra loro.

### percorso ibrido:

```
import("stdfaust.lib");
process = +,+:+;
```

![parallelo](https://raw.githubusercontent.com/LSSN/appunti/master/code/ibrido-svg/process.png)

Il programma esegue la somma di quattro segnali.

## regole base

Una riga di commento deve iniziare con `//` e non può essere interrotta.

Ogni programma deve avere le seguenti righe:

```
import("stdfaust.lib");
process = scrivi qui il tuo programma;
```

Ogni programma può avere una sola riga `process`.

Ogni riga termina con un `;`

## diagramma di flusso

Un digramma di flusso indica il percorso dei segnali ed i processi ad essi applicati.

![diagramma](https://raw.githubusercontent.com/LSSN/appunti/master/code/diagramma-svg/process.png)

Il programma esegue una somma dei due segnali in entrata e poi una moltiplicazione per una costante.


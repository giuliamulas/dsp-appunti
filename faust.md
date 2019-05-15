# FAUST

## operatori matematici

`+ – * /`

## gestione segnali

`_` (trattino basso, identifica il segnale audio)

`:` (identificano un percorso seriale, ovvero in sequenza)

`,` (identifica un percorso parallelo)

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

esempio di digramma di flusso.

abbiamo due segnali in entrata che vengono sommati tra loro e poi moltiplicati per una costante.

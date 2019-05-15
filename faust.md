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

process = _ ;

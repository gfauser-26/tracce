# E06 - Inverti la lista

- **Livello:** sfida
- **Lezione:** Memoria: stack, heap e puntatori (ven 30/10/2026)
- **Cartella della consegna:** `informatica/2026-27/esercizi/E06-2026-10-30-inverti-lista/`
- **Linguaggio:** quello scelto da te (`lang.txt`), uno degli otto ammessi.
- **Scadenza:** la fissa il docente in classe (giorno e ora).

## Cosa fare

Leggi dei numeri e mettili in una lista concatenata **nello stesso ordine di lettura** (in coda). Poi **inverti la lista cambiando i collegamenti**, senza creare nodi nuovi e senza copiare i valori in un vettore. Stampa la lista prima e dopo.

## Regole

- Per invertire servono tre riferimenti: il nodo precedente, il corrente e il successivo. Disegna i frammenti prima di scrivere.
- Niente vettori né liste del linguaggio per tenere i dati.

## Ingresso

- Numeri interi separati da spazi o a capo, fino alla fine dell'ingresso (può essere vuoto).

## Uscita

- `prima: a -> b -> c -> fine`
- `dopo: c -> b -> a -> fine`
- Con la lista vuota: `prima: fine` e `dopo: fine`.

## Esempio

Ingresso:

```text
1 2 3
```

Uscita attesa:

```text
prima: 1 -> 2 -> 3 -> fine
dopo: 3 -> 2 -> 1 -> fine
```

## Suggerimenti

- Cosa succede al nodo di testa? E alla coda dopo l'inversione?
- Ripassa a mano l'inversione su una lista di 3 nodi, disegnando le frecce a ogni passo.

## Come si controlla

- Il programma legge da **standard input** e scrive su **standard output**; niente messaggi del tipo «Inserisci...».
- Provalo con `fauser test`: usa i 3 casi pubblici di `tests/`. Il docente rifà girare anche altri casi che non vedi (valori limite, ingressi vuoti, numeri negativi): pensa ai casi particolari.
- Nel `README.md` scrivi come hai pensato la soluzione e come hai usato l'AI (se l'hai usata).

# E04 - Il vettore che cresce

- **Livello:** base
- **Lezione:** Memoria: stack, heap e puntatori (ven 30/10/2026)
- **Cartella della consegna:** `informatica/2026-27/esercizi/E04-2026-10-30-vettore-che-cresce/`
- **Linguaggio:** quello scelto da te (`lang.txt`), uno degli otto ammessi.
- **Scadenza:** la fissa il docente in classe (giorno e ora).

## Cosa fare

Leggi dei numeri **senza sapere quanti sono**: finiscono quando arriva 0. Tienili in un vettore che si allarga da solo (in C: `malloc` e `realloc`, e alla fine `free`; negli altri linguaggi la lista del linguaggio). Poi calcola il massimo e quali numeri stanno sopra la media.

## Regole

- Il numero 0 chiude l'ingresso e **non** fa parte dei dati.
- «Sopra la media» vuol dire `x * n > somma`, dove `n` è quanti numeri hai letto e `somma` è la loro somma (così non servono i decimali).
- I numeri possono essere negativi.

## Ingresso

- Numeri interi separati da spazi o a capo, fino al primo 0 (che chiude). Quello che viene dopo lo 0 si ignora.

## Uscita

- `Letti: n`.
- Se `n` è 0, ti fermi qui.
- Altrimenti `Massimo: m` e poi `Sopra la media: ` seguito dai numeri sopra la media **nell'ordine di lettura**, uno dopo l'altro separati da uno spazio; se non ce n'è nessuno, `Sopra la media: nessuno`.

## Esempio

Ingresso:

```text
5 3 8 1 9 0
```

Uscita attesa:

```text
Letti: 5
Massimo: 9
Sopra la media: 8 9
```

## Suggerimenti

- In C parti con capacità 4 e raddoppia quando serve; non indovinare un massimo (niente `int v[1000]`).
- Ci sono test con mille numeri: se il tuo vettore non cresce, lo scopri subito.

## Come si controlla

- Il programma legge da **standard input** e scrive su **standard output**; niente messaggi del tipo «Inserisci...».
- Provalo con `fauser test`: usa i 3 casi pubblici di `tests/`. Il docente rifà girare anche altri casi che non vedi (valori limite, ingressi vuoti, numeri negativi): pensa ai casi particolari.
- Nel `README.md` scrivi come hai pensato la soluzione e come hai usato l'AI (se l'hai usata).

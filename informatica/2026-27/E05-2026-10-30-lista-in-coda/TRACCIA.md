# E05 - Lista in coda

- **Livello:** intermedio
- **Lezione:** Memoria: stack, heap e puntatori (ven 30/10/2026)
- **Cartella della consegna:** `informatica/2026-27/esercizi/E05-2026-10-30-lista-in-coda/`
- **Linguaggio:** quello scelto da te (`lang.txt`), uno degli otto ammessi.
- **Scadenza:** la fissa il docente in classe (giorno e ora).

## Cosa fare

Costruisci una **lista concatenata** di numeri interi, con una classe (o struct) `Nodo` che contiene un valore e il riferimento al nodo successivo. A differenza dell'esempio visto a lezione (inserimento in testa), qui si inserisce **in coda**. Il programma esegue dei comandi.

## Regole

- **Non usare** vettori, `List`, array dinamici o liste del linguaggio per tenere i dati: devono stare nei nodi collegati. (Il docente lo controlla leggendo il codice.)
- In C: ricordati di `free` di tutti i nodi prima di uscire.

## Ingresso

Comandi, uno per riga, fino a `Q`:
- `A x`: aggiungi `x` in coda.
- `C x`: contiene `x`?
- `P`: stampa la lista.
- `N`: quanti nodi.
- `Q`: fine.

## Uscita

- `A`: niente.
- `C x`: `si` oppure `no`.
- `P`: `a -> b -> c -> fine` (con la lista vuota: solo `fine`).
- `N`: il numero.

## Esempio

Ingresso:

```text
A 5
A 7
P
C 7
C 8
N
Q
```

Uscita attesa:

```text
5 -> 7 -> fine
si
no
2
```

## Suggerimenti

- Per aggiungere in coda scorri fino all'ultimo nodo (quello con `prossimo` nullo). Con la lista vuota la testa è nulla: caso a parte.
- Disegna su carta 0, 1 e 2 nodi prima di scrivere il codice.

## Come si controlla

- Il programma legge da **standard input** e scrive su **standard output**; niente messaggi del tipo «Inserisci...».
- Provalo con `fauser test`: usa i 3 casi pubblici di `tests/`. Il docente rifà girare anche altri casi che non vedi (valori limite, ingressi vuoti, numeri negativi): pensa ai casi particolari.
- Nel `README.md` scrivi come hai pensato la soluzione e come hai usato l'AI (se l'hai usata).

# E02 · Magazzino semplice

- **Materia:** TPSIT, anno scolastico 2027-28 · **L01** (slot 1 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-13) · slide: `materiali/tpsit5/p32/L01-dal-csharp-a-java/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E02-2027-09-13-magazzino-semplice/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un magazzino tiene la **giacenza** di alcuni articoli. Un articolo non ancora visto ha giacenza 0.

## Ingresso

Un comando per riga: `carico nome n`, `scarico nome n`, `giacenza nome`. I nomi sono una parola, le quantità interi positivi.

## Uscita

Per `giacenza`: `nome n`. Se uno `scarico` supera la giacenza stampa `insufficiente nome` e non cambia nulla.

## Vincoli

Una classe `Articolo` (nome e quantità) e un elenco di articoli; la ricerca per nome è lineare, la mappa arriva nella lezione 3.

## Esempio

Ingresso:

```text
carico penna 10
scarico penna 3
giacenza penna
```

Uscita:

```text
penna 7
```

## Come si lavora

1. `fauser nuovo E02 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

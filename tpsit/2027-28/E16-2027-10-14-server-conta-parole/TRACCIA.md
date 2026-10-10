# E16 · Server che conta le parole

- **Materia:** TPSIT, anno scolastico 2027-28 · **L10** (slot 10 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-14) · slide: `materiali/tpsit5/p32/L10-tcp-in-java/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E16-2027-10-14-server-conta-parole/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Come l'echo di E15 (client e server nello stesso programma, socket TCP veri su `127.0.0.1`), ma il server risponde con il **numero di parole** della riga.

## Ingresso

Righe di testo (anche vuote).

## Uscita

Una riga per ogni riga di ingresso, con il numero di parole (0 per una riga vuota).

## Vincoli

Le parole sono separate da uno o più spazi.

## Esempio

Ingresso:

```text
il gatto e il cane
```

Uscita:

```text
5
```

## Come si lavora

1. `fauser nuovo E16 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

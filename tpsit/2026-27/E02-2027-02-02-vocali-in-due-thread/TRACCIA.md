# E02 · Vocali in due thread

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA3 Processi e thread**
- **Lezione:** 4BIN n. 30 (mar 02/02), 4DIN n. 18 (lun 01/03) · slide: `materiali/tpsit4/p32/thread-seq-par/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E02-2027-02-02-vocali-in-due-thread/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Leggi **una riga** di testo. Due thread contano le **vocali** (a, e, i, o, u, maiuscole o minuscole): il primo nella prima metà della riga (caratteri da `0` a `lunghezza / 2 - 1`), il secondo nel resto. Dopo il `join` stampa i tre numeri.

## Ingresso

Una riga di testo (lettere, spazi, punteggiatura; niente lettere accentate).

## Uscita

Tre righe: `prima meta: X`, `seconda meta: Y`, `totale: Z`.

## Vincoli

1 <= lunghezza <= 2000. La metà si calcola con la divisione intera.

## Esempio

Ingresso:

```text
Ciao mondo
```

Uscita:

```text
prima meta: 3
seconda meta: 2
totale: 5
```

## Come si lavora

1. `fauser nuovo E02 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

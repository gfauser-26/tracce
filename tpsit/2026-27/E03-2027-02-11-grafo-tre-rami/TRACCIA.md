# E03 · Grafo con tre rami

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA3 Processi e thread**
- **Lezione:** 4BIN n. 32 (gio 11/02, come compito), 4DIN n. 16 (lun 15/02) · slide: `materiali/tpsit4/p32/grafo-fork-join-cobegin/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E03-2027-02-11-grafo-tre-rami/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Traduci in codice questo **grafo delle precedenze**: `S1`, poi `S2`, `S3` e `S4` **in parallelo**, poi `S5`.

- `S1`: `a = x + 1`
- `S2`: `b = a * 2`
- `S3`: `c = a * a`
- `S4`: `d = a - 3`
- `S5`: `e = b + c + d`

Usa fork-join oppure cobegin-coend (a scelta, scrivilo nel README). `S5` parte solo dopo che `S2`, `S3` e `S4` sono finiti.

## Ingresso

Un intero `x`.

## Uscita

Cinque righe: `a = ...`, `b = ...`, `c = ...`, `d = ...`, `e = ...`.

## Vincoli

-1000 <= x <= 1000. I tre rami scrivono variabili diverse.

## Esempio

Ingresso:

```text
3
```

Uscita:

```text
a = 4
b = 8
c = 16
d = 1
e = 25
```

## Come si lavora

1. `fauser nuovo E03 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

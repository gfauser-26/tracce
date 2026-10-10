# C03 · Righe vuote e righe lunghe

- **Materia:** TPSIT, anno scolastico 2027-28 · **L03** (slot 3 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-20) · slide: `materiali/tpsit5/p32/L03-collezioni-e-generics/`
- **Compito della lezione 03**, per preparare la lezione 04 · I/O in Java: file, stream, serializzazione.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C03-2027-09-20-righe-vuote-e-lunghe/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Leggi il testo dallo standard input **riga per riga** e conta le righe totali, quelle **vuote** (solo spazi o niente) e quelle **lunghe** (più di 20 caratteri).

## Ingresso

Testo su più righe.

## Uscita

Una riga: `righe R vuote V lunghe L`.

## Vincoli

Prepara la lezione 4: nota come leggi una riga alla volta e come riconosci la fine dell'input.

## Esempio

Ingresso:

```text
ciao

una riga davvero molto lunga
```

Uscita:

```text
righe 3 vuote 1 lunghe 1
```

## Come si lavora

1. `fauser nuovo C03 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

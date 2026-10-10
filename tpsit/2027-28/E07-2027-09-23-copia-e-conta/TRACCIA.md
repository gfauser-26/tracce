# E07 · Copia e conta

- **Materia:** TPSIT, anno scolastico 2027-28 · **L04** (slot 4 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-23) · slide: `materiali/tpsit5/p32/L04-io-file-stream-serializzazione/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E07-2027-09-23-copia-e-conta/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Leggi tutte le righe dello standard input e **salvale in un file temporaneo**. Poi **rileggi il file** e conta le righe, le parole (separate da spazi) e i caratteri (esclusi gli a capo).

## Ingresso

Testo su più righe. L'ultima riga può non avere l'a capo finale.

## Uscita

Una riga: `righe R parole P caratteri C`.

## Vincoli

Usa un file temporaneo del tuo linguaggio, chiudilo prima di rileggerlo e cancellalo alla fine. Chiudi sempre il file (try-with-resources, `with`, `defer`).

## Esempio

Ingresso:

```text
prima riga
seconda
```

Uscita:

```text
righe 2 parole 3 caratteri 17
```

## Come si lavora

1. `fauser nuovo E07 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

# E08 · Registro in CSV

- **Materia:** TPSIT, anno scolastico 2027-28 · **L04** (slot 4 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-23) · slide: `materiali/tpsit5/p32/L04-io-file-stream-serializzazione/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E08-2027-09-23-registro-csv/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Ogni riga descrive un articolo venduto: `nome;quantità;prezzo`, con il prezzo in **centesimi**. Per ogni riga stampa il totale (quantità per prezzo) e alla fine il totale generale.

## Ingresso

Righe `nome;quantita;prezzo` (interi positivi). Le righe vuote si ignorano.

## Uscita

Per ogni riga `nome totale`; ultima riga `totale T`.

## Vincoli

Spezza la riga con il separatore `;` (`split(";")`). Non usare numeri decimali: tutto in centesimi.

## Esempio

Ingresso:

```text
penna;3;150
quaderno;2;300
```

Uscita:

```text
penna 450
quaderno 600
totale 1050
```

## Come si lavora

1. `fauser nuovo E08 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

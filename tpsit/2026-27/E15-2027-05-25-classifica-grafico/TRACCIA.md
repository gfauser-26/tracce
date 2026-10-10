# E15 · Classifica per il grafico

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA6 Frontend data-driven e React**
- **Lezione:** 4BIN n. 59 (mar 25/05), 4DIN n. 28 (lun 17/05, facoltativo) · slide: `materiali/tpsit4/p32/chartjs/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E15-2027-05-25-classifica-grafico/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Prepara i dati per un **grafico a barre ordinato**. Leggi `n` righe `etichetta valore` e ordinale per valore **decrescente**: a parità di valore resta l'ordine di ingresso. Stampa le etichette, i valori, il totale e le percentuali (parte intera di `100 * valore / totale`).

## Ingresso

Prima riga: `n`. Poi `n` righe `etichetta valore` (etichetta senza spazi).

## Uscita

Quattro righe: `labels: ...`, `valori: ...`, `totale: T`, `percentuali: ...` (liste separate da virgola, senza spazi).

## Vincoli

1 <= n <= 50; valori interi >= 0; il totale è > 0.

## Esempio

Ingresso:

```text
3
gen 120
feb 95
mar 150
```

Uscita:

```text
labels: mar,gen,feb
valori: 150,120,95
totale: 365
percentuali: 41,32,26
```

## Come si lavora

1. `fauser nuovo E15 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

## Nota

Ordine stabile: a pari valore vince chi è arrivato prima.

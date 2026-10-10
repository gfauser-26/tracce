# E01 · Massimo in due thread

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA3 Processi e thread**
- **Lezione:** 4BIN n. 30 (mar 02/02), 4DIN n. 18 (lun 01/03) · slide: `materiali/tpsit4/p32/thread-seq-par/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E01-2027-02-02-massimo-in-due-thread/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Leggi `n` numeri interi. Fai partire **due thread**: il primo cerca il massimo tra i primi `n / 2` numeri (indici da `0` a `n/2 - 1`), il secondo tra i restanti. Aspetta i due thread (`join`) e solo **dopo** stampa i risultati.

## Ingresso

Prima riga: `n`. Seconda riga: gli `n` numeri separati da spazio.

## Uscita

Tre righe: `meta 1: M1`, `meta 2: M2`, `massimo: M` (M è il più grande dei due).

## Vincoli

2 <= n <= 1000; numeri tra -10000 e 10000. Un thread per metà: niente stampe dentro i thread.

## Esempio

Ingresso:

```text
5
3 9 -2 7 1
```

Uscita:

```text
meta 1: 9
meta 2: 7
massimo: 9
```

## Come si lavora

1. `fauser nuovo E01 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

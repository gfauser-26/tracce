# E04 · Cobegin: conteggi

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA3 Processi e thread**
- **Lezione:** 4BIN n. 32 (gio 11/02, come compito), 4DIN n. 16 (lun 15/02) · slide: `materiali/tpsit4/p32/grafo-fork-join-cobegin/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E04-2027-02-11-cobegin-conteggi/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Leggi `n` interi. In un blocco **cobegin-coend** fai partire tre rami che scorrono lo stesso vettore: uno conta i numeri **positivi**, uno i **negativi**, uno gli **zeri**. Alla fine (dopo il coend) stampa i tre conteggi.

## Ingresso

Prima riga: `n`. Seconda riga: gli `n` numeri.

## Uscita

Tre righe: `positivi: P`, `negativi: N`, `zeri: Z`.

## Vincoli

1 <= n <= 1000. Ogni ramo scrive solo la sua variabile.

## Esempio

Ingresso:

```text
6
3 -1 0 5 0 -2
```

Uscita:

```text
positivi: 2
negativi: 2
zeri: 2
```

## Come si lavora

1. `fauser nuovo E04 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

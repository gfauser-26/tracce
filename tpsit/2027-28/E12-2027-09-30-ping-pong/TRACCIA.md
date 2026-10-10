# E12 · Ping e pong con i semafori

- **Materia:** TPSIT, anno scolastico 2027-28 · **L06** (slot 6 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-30) · slide: `materiali/tpsit5/p32/L06-executor-lock-semafori/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E12-2027-09-30-ping-pong/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Due thread stampano `ping` e `pong` **alternati**, per `N` volte ciascuno, usando **due semafori**.

## Ingresso

Un intero `N`.

## Uscita

`2N` righe: `ping`, `pong`, `ping`, `pong`, ...

## Vincoli

Il semaforo di ping parte a 1, quello di pong a 0. Ogni thread aspetta il proprio e dà il via all'altro.

## Esempio

Ingresso:

```text
1
```

Uscita:

```text
ping
pong
```

## Come si lavora

1. `fauser nuovo E12 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

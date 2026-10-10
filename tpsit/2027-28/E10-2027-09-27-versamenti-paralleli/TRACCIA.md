# E10 · Versamenti e prelievi in parallelo

- **Materia:** TPSIT, anno scolastico 2027-28 · **L05** (slot 5 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-27) · slide: `materiali/tpsit5/p32/L05-thread-in-java/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E10-2027-09-27-versamenti-paralleli/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un conto parte da 0. `D` thread versano ciascuno 2 euro per `K` volte; `P` thread prelevano ciascuno 1 euro per `K` volte. Il saldo può scendere sotto zero durante l'esecuzione. Stampa il saldo finale: **deve essere esatto**.

## Ingresso

Una riga con `D P K`.

## Uscita

`saldo X`.

## Vincoli

Un solo lucchetto condiviso per tutte le operazioni sul saldo. Senza lucchetto il risultato cambia da una esecuzione all'altra.

## Esempio

Ingresso:

```text
2 1 1000
```

Uscita:

```text
saldo 3000
```

## Come si lavora

1. `fauser nuovo E10 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

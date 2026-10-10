# E20 · Fattoriali per molti client

- **Materia:** TPSIT, anno scolastico 2027-28 · **L12** (slot 12 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-21) · slide: `materiali/tpsit5/p32/L12-server-multithread/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E20-2027-10-21-fattoriali-clienti/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un server TCP calcola il **fattoriale**. Lanci un client per ogni numero, tutti in contemporanea; ogni client spedisce il suo numero e legge la risposta. Il programma stampa i risultati **nell'ordine di ingresso**.

## Ingresso

Una riga con `K`, poi `K` interi da 0 a 20.

## Uscita

Per ogni numero `n fattoriale`.

## Vincoli

Il fattoriale di 20 non sta in 32 bit: usa interi a 64 bit (`long`, `int64`, `BigInt` in TypeScript).

## Esempio

Ingresso:

```text
3
3 4 5
```

Uscita:

```text
3 6
4 24
5 120
```

## Come si lavora

1. `fauser nuovo E20 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

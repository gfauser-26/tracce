# E21 · Crociera: vendita dei posti

- **Materia:** TPSIT, anno scolastico 2027-28 · **L13** (slot 13 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-25) · slide: `materiali/tpsit5/p32/L13-crociera-posti-limitati/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E21-2027-10-25-crociera-posti/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un server TCP vende biglietti per la crociera: ci sono `P` posti. Lanci `K` client in contemporanea; ognuno manda `BUY` e riceve `OK` o `COMPLETO`. Alla fine stampa quanti biglietti ha venduto e rifiutati e quanti posti restano.

## Ingresso

Una riga: `P K`.

## Uscita

Tre righe: `venduti V`, `rifiutati R`, `posti S`.

## Vincoli

Controllo e vendita devono essere un **blocco solo** protetto dal lucchetto. Il risultato non dipende dall'ordine di arrivo dei client.

## Esempio

Ingresso:

```text
3 5
```

Uscita:

```text
venduti 3
rifiutati 2
posti 0
```

## Come si lavora

1. `fauser nuovo E21 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

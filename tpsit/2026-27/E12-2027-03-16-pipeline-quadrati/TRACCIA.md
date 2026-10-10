# E12 · Catena in tre stadi

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA5 Comunicazione e sincronizzazione**
- **Lezione:** 4BIN n. 41 (mar 16/03), 4DIN n. 23 (lun 12/04) · slide: `materiali/tpsit4/p32/produttori-consumatori/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E12-2027-03-16-pipeline-quadrati/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Tre thread in catena, con **due buffer** da `b` celle: lo stadio 1 produce `1, 2, ..., n`; lo stadio 2 prende ogni numero, lo **eleva al quadrato** e lo passa avanti; lo stadio 3 **somma** i quadrati. Alla fine stampa quanti elementi sono passati e la somma.

## Ingresso

Una riga: `n b`.

## Uscita

Due righe: `elementi: N` e `somma dei quadrati: S`.

## Vincoli

1 <= n <= 1000; 1 <= b <= 16. La somma entra in 64 bit.

## Esempio

Ingresso:

```text
5 2
```

Uscita:

```text
elementi: 5
somma dei quadrati: 55
```

## Come si lavora

1. `fauser nuovo E12 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

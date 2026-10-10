# E14 · Coda di messaggi

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA5 Comunicazione e sincronizzazione**
- **Lezione:** 4BIN n. 44 (gio 01/04) · slide: `materiali/tpsit4/p32/lettori-scrittori/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E14-2027-04-01-coda-messaggi/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Modello ad **ambiente locale**: due thread che **non condividono variabili**. Il **mittente** manda gli `n` numeri letti uno alla volta in una **coda di messaggi** (coda bloccante o canale); il **destinatario** li riceve e calcola somma e massimo. Alla fine (dopo il `join`) stampa quanti messaggi sono arrivati, la somma e il massimo.

## Ingresso

Prima riga: `n`. Seconda riga: gli `n` numeri.

## Uscita

Tre righe: `messaggi: N`, `somma: S`, `massimo: M`.

## Vincoli

1 <= n <= 1000. Niente variabili globali scritte da entrambi: l'unico canale è la coda (il risultato lo restituisce il destinatario).

## Esempio

Ingresso:

```text
5
3 -1 4 1 5
```

Uscita:

```text
messaggi: 5
somma: 12
massimo: 5
```

## Come si lavora

1. `fauser nuovo E14 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

# E19 · Contatore condiviso nel server

- **Materia:** TPSIT, anno scolastico 2027-28 · **L12** (slot 12 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-21) · slide: `materiali/tpsit5/p32/L12-server-multithread/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E19-2027-10-21-contatore-server/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un server TCP (socket veri su `127.0.0.1`, porta 0) tiene un **contatore condiviso**. Lanci `K` client in contemporanea; ognuno manda `M` volte la riga `INC` (il server non risponde a `INC`). Quando tutti hanno finito, un ultimo client manda `TOTALE` e il server risponde con il valore.

## Ingresso

Una riga: `K M`.

## Uscita

Una riga `totale N`, dove `N` deve essere esattamente `K` per `M`.

## Vincoli

Il server serve ogni client in un thread: il contatore va protetto con un lucchetto. Senza lucchetto il totale è minore del dovuto.

## Esempio

Ingresso:

```text
3 100
```

Uscita:

```text
totale 300
```

## Come si lavora

1. `fauser nuovo E19 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

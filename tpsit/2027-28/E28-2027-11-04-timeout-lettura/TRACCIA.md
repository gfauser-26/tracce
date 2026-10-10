# E28 · Timeout di lettura

- **Materia:** TPSIT, anno scolastico 2027-28 · **L16** (slot 16 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-11-04) · slide: `materiali/tpsit5/p32/L16-pool-timeout-collaudo/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E28-2027-11-04-timeout-lettura/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un server TCP (socket veri su `127.0.0.1`, porta 0, pool di 2 lavoratori) risponde `ok` dopo un **ritardo** in millisecondi che il client gli manda. Il client aspetta al massimo `T` millisecondi: se la risposta non arriva stampa `timeout`, altrimenti `risposta`. Alla fine il server si chiude in modo ordinato e il programma stampa `chiuso`.

## Ingresso

Una riga con `T`, poi i ritardi (uno per riga o separati da spazio). Ritardi e `T` differiscono sempre di almeno 200 ms.

## Uscita

Per ogni ritardo `risposta` o `timeout`, poi `chiuso`.

## Vincoli

Imposta il timeout **sul socket** (`setSoTimeout`, `ReadTimeout`, `settimeout`, `SetReadDeadline`), non con uno sleep del client.

## Esempio

Ingresso:

```text
400
20
1000
```

Uscita:

```text
risposta
timeout
chiuso
```

## Come si lavora

1. `fauser nuovo E28 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

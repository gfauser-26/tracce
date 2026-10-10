# C04 · Metà e metà

- **Materia:** TPSIT, anno scolastico 2027-28 · **L04** (slot 4 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-23) · slide: `materiali/tpsit5/p32/L04-io-file-stream-serializzazione/`
- **Compito della lezione 04**, per preparare la lezione 05 · Thread in Java.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C04-2027-09-23-meta-e-meta/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Leggi `N` numeri e calcola la somma della **prima metà** (i primi `N/2`, divisione intera) e della **seconda metà** (gli altri), **in sequenza**, senza thread. Nella lezione 5 affiderai ogni metà a un thread.

## Ingresso

Una riga con `N`, poi `N` numeri (anche su più righe).

## Uscita

Tre righe: `prima A`, `seconda B`, `totale T`.

## Vincoli

Prepara la lezione 5: ripassa il grafo delle precedenze della quarta.

## Esempio

Ingresso:

```text
4
1 2 3 4
```

Uscita:

```text
prima 3
seconda 7
totale 10
```

## Come si lavora

1. `fauser nuovo C04 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

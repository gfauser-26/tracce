# E09 · Somma in T thread

- **Materia:** TPSIT, anno scolastico 2027-28 · **L05** (slot 5 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-27) · slide: `materiali/tpsit5/p32/L05-thread-in-java/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E09-2027-09-27-somma-in-t-thread/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Leggi `T` e `N`, poi `N` numeri. Dividi i numeri in `T` blocchi: il blocco `i` (da 0 a T-1) contiene gli elementi con indice da `i*N/T` incluso a `(i+1)*N/T` escluso (divisione intera). **Un thread per blocco** somma il suo pezzo; il thread principale aspetta tutti e stampa i parziali e il totale.

## Ingresso

Una riga con `T N`, poi gli `N` numeri (anche su più righe). `1 ≤ T ≤ 8`.

## Uscita

`parziale i S` per i da 1 a T, in ordine, poi `somma S`.

## Vincoli

Ogni thread scrive in una posizione diversa di un vettore dei parziali: non serve un lucchetto, serve il `join`.

## Esempio

Ingresso:

```text
2 4
1 2 3 4
```

Uscita:

```text
parziale 1 3
parziale 2 7
somma 10
```

## Come si lavora

1. `fauser nuovo E09 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

# E06 · Minimo in parallelo

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA3 Processi e thread**
- **Lezione:** 4BIN n. 33 (mar 16/02), 4DIN n. 19 (lun 08/03) · slide: `materiali/tpsit4/p32/prestazioni-tempi/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E06-2027-02-16-minimo-parallelo/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Trova il **minimo** di un vettore con `k` thread: ogni thread cerca nella sua fetta (da `i * n / k` a `(i + 1) * n / k`, esclusa) e scrive il risultato nel **suo** posto. Le fette **vuote** (se `k > n`) vanno saltate. Confronta con il minimo sequenziale. Il tempo va su stderr.

## Ingresso

Prima riga: `n k`. Seconda riga: gli `n` numeri.

## Uscita

Tre righe: `minimo sequenziale: M`, `minimo parallelo (K thread): M`, `uguali: si`.

## Vincoli

1 <= n <= 100000; 1 <= k <= 16.

## Esempio

Ingresso:

```text
5 2
8 3 9 -4 6
```

Uscita:

```text
minimo sequenziale: -4
minimo parallelo (2 thread): -4
uguali: si
```

## Come si lavora

1. `fauser nuovo E06 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

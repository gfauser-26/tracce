# E11 · N produttori e M consumatori

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA5 Comunicazione e sincronizzazione**
- **Lezione:** 4BIN n. 41 (mar 16/03), 4DIN n. 23 (lun 12/04) · slide: `materiali/tpsit4/p32/produttori-consumatori/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E11-2027-03-16-produttori-consumatori-nxm/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

`n` produttori e `m` consumatori condividono un buffer di `b` celle. Ogni produttore produce i valori `1, 2, ..., k`. I consumatori, tutti insieme, consumano tutti gli oggetti: ognuno ne consuma esattamente `n * k / m`. Usa **semafori** (celle libere, celle piene) e un **mutex** per gli indici. Alla fine stampa quanti oggetti sono stati prodotti, consumati e la loro somma.

## Ingresso

Una riga: `n m b k`.

## Uscita

Tre righe: `prodotti: P`, `consumati: C`, `somma: S` (P = C = n * k; S = n * k * (k + 1) / 2).

## Vincoli

1 <= n, m <= 8; 1 <= b <= 32; 1 <= k <= 200; **n * k è divisibile per m**.

## Esempio

Ingresso:

```text
2 2 3 5
```

Uscita:

```text
prodotti: 10
consumati: 10
somma: 30
```

## Come si lavora

1. `fauser nuovo E11 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

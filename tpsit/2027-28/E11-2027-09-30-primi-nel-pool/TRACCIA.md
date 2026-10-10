# E11 · Numeri primi nel pool

- **Materia:** TPSIT, anno scolastico 2027-28 · **L06** (slot 6 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-30) · slide: `materiali/tpsit5/p32/L06-executor-lock-semafori/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E11-2027-09-30-primi-nel-pool/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Stabilisci se ciascun numero è primo, affidando i controlli a un **pool di 4 lavoratori**. I risultati si stampano **nell'ordine di ingresso**, non in quello di arrivo.

## Ingresso

Una riga con `N`, poi `N` numeri interi non negativi (anche su più righe).

## Uscita

Per ogni numero `n primo` oppure `n non primo`. 0 e 1 non sono primi.

## Vincoli

Divisione per tentativi fino alla radice quadrata (niente algoritmi sofisticati). Ricordati di chiudere il pool.

## Esempio

Ingresso:

```text
5
2 3 4 5 6
```

Uscita:

```text
2 primo
3 primo
4 non primo
5 primo
6 non primo
```

## Come si lavora

1. `fauser nuovo E11 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

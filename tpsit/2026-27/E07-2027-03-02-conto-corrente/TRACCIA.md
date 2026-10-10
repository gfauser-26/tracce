# E07 · Il conto corrente

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA5 Comunicazione e sincronizzazione**
- **Lezione:** 4BIN n. 37 (mar 02/03), 4DIN n. 21 (lun 22/03) · slide: `materiali/tpsit4/p32/interleaving-lock/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E07-2027-03-02-conto-corrente/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un conto parte con **100** euro. `k` thread lavorano sullo stesso conto: ognuno ripete `m` volte «**versa 3**, poi **preleva 2**». Proteggi il saldo con un **lock** (o monitor). Alla fine, dopo il `join`, stampa il saldo e quello atteso.

## Ingresso

Una riga: `k m`.

## Uscita

Due righe: `saldo: S` e `atteso: A` (A = 100 + k * m).

## Vincoli

1 <= k <= 16; 1 <= m <= 100000. Senza lock il saldo non torna (a volte sì).

## Esempio

Ingresso:

```text
2 5
```

Uscita:

```text
saldo: 110
atteso: 110
```

## Come si lavora

1. `fauser nuovo E07 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

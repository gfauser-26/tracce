# E04 · Conto risparmio con limite di prelievi

- **Materia:** TPSIT, anno scolastico 2027-28 · **L02** (slot 2 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-16) · slide: `materiali/tpsit5/p32/L02-oop-in-java/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E04-2027-09-16-conto-risparmio/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un `ContoRisparmio` **estende** il conto: permette al massimo **3 prelievi riusciti**. Dal quarto, ogni prelievo è rifiutato con `limite prelievi`. Un prelievo oltre il saldo è `rifiutato` e **non** conta come prelievo.

## Ingresso

Un comando per riga: `versa N`, `preleva N`, `saldo`.

## Uscita

`saldo X` per ogni `saldo`; `rifiutato` o `limite prelievi` per i prelievi non eseguiti. Il controllo del limite viene prima del controllo del saldo.

## Vincoli

La classe figlia riscrive solo `preleva`.

## Esempio

Ingresso:

```text
versa 100
preleva 10
preleva 10
preleva 10
preleva 10
saldo
```

Uscita:

```text
limite prelievi
saldo 70
```

## Come si lavora

1. `fauser nuovo E04 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

# E16 · Somme mobili

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA6 Frontend data-driven e React**
- **Lezione:** 4BIN n. 59 (mar 25/05), 4DIN n. 28 (lun 17/05, facoltativo) · slide: `materiali/tpsit4/p32/chartjs/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E16-2027-05-25-somme-mobili/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Per **addolcire** una linea di un grafico si usa una finestra mobile. Leggi `n` numeri e una larghezza `w`; per ogni posizione stampa la **somma** dei `w` numeri consecutivi che iniziano lì (solo le finestre complete).

## Ingresso

Prima riga: `n w`. Seconda riga: gli `n` numeri.

## Uscita

Una riga: `somme: ` seguita dalle `n - w + 1` somme separate da uno spazio.

## Vincoli

1 <= w <= n <= 1000.

## Esempio

Ingresso:

```text
5 2
1 2 3 4 5
```

Uscita:

```text
somme: 3 5 7 9
```

## Come si lavora

1. `fauser nuovo E16 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

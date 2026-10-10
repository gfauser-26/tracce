# E05 · Elementi distinti, due costi

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA3 Processi e thread**
- **Lezione:** 4BIN n. 33 (mar 16/02), 4DIN n. 19 (lun 08/03) · slide: `materiali/tpsit4/p32/prestazioni-tempi/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E05-2027-02-16-elementi-distinti/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Quanti numeri **diversi** ci sono in un vettore? Scrivi **due versioni**: (1) con due cicli annidati (confronti ogni numero con i precedenti), (2) ordinando il vettore e contando i cambi di valore. Stampa i due risultati e se coincidono. I **tempi** delle due versioni vanno su **stderr** (non nell'uscita standard).

## Ingresso

Prima riga: `n`. Seconda riga: gli `n` numeri.

## Uscita

Tre righe: `versione quadratica: D`, `versione con ordinamento: D`, `uguali: si` (o `no`).

## Vincoli

1 <= n <= 5000. Prova con n grande e guarda i due tempi: quale cresce più in fretta?

## Esempio

Ingresso:

```text
6
4 7 4 1 7 9
```

Uscita:

```text
versione quadratica: 4
versione con ordinamento: 4
uguali: si
```

## Come si lavora

1. `fauser nuovo E05 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

## Nota

I tempi non sono verificati dai test: lo scopo è vederli.

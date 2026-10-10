# E22 · Crociera con due classi di biglietto

- **Materia:** TPSIT, anno scolastico 2027-28 · **L13** (slot 13 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-25) · slide: `materiali/tpsit5/p32/L13-crociera-posti-limitati/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E22-2027-10-25-crociera-classi/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Due classi: `E` (economy, 100 euro) e `B` (balcone, 150 euro), con `PE` e `PB` posti. Lanci `K` client in contemporanea; ognuno chiede una classe e riceve `OK` o `COMPLETO`. Alla fine stampa venduti e incasso per classe e l'incasso totale.

## Ingresso

Una riga con `PE PB K`, poi `K` lettere `E` o `B` (separate da spazi, anche su più righe).

## Uscita

Tre righe: `economy V I`, `balcone V I`, `totale T`.

## Vincoli

Un solo lucchetto per tutte e due le classi è la scelta più semplice. Gli importi sono interi.

## Esempio

Ingresso:

```text
2 1 5
E E E B B
```

Uscita:

```text
economy 2 200
balcone 1 150
totale 350
```

## Come si lavora

1. `fauser nuovo E22 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

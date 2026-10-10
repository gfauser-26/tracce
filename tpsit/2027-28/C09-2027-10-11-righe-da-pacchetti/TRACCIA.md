# C09 · Righe da pacchetti

- **Materia:** TPSIT, anno scolastico 2027-28 · **L09** (slot 9 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-11) · slide: `materiali/tpsit5/p32/L09-client-server-e-socket/`
- **Compito della lezione 09**, per preparare la lezione 10 · TCP in Java.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C09-2027-10-11-righe-da-pacchetti/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

TCP consegna un **flusso di byte** a pezzi. Ogni riga di ingresso è un pezzo (*pacchetto*) di flusso, nel quale il carattere `|` rappresenta un **a capo**. Ricomponi il flusso e stampa le righe **complete** non appena sono complete. Se alla fine resta del testo senza a capo, stampalo come `resto: testo`.

## Ingresso

Pacchetti, uno per riga. Un pacchetto può contenere zero, uno o più `|`.

## Uscita

Una riga per ogni riga completa, poi (se serve) `resto: testo`.

## Vincoli

Prepara la lezione 10: capisci perché una riga di testo non coincide con un pacchetto.

## Esempio

Ingresso:

```text
cia
o|mon
do|
```

Uscita:

```text
ciao
mondo
```

## Come si lavora

1. `fauser nuovo C09 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

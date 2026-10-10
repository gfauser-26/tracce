# E03 · Perimetri e triangoli non validi

- **Materia:** TPSIT, anno scolastico 2027-28 · **L02** (slot 2 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-16) · slide: `materiali/tpsit5/p32/L02-oop-in-java/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E03-2027-09-16-perimetri/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Riprendi le forme della lezione: ogni forma ha un metodo `perimetro()`. Un triangolo è valido solo se **ogni lato è minore della somma degli altri due**; altrimenti è un errore che il programma segnala con un'eccezione (o con l'errore del tuo linguaggio) e stampa come testo.

## Ingresso

Una forma per riga: `rettangolo a b`, `quadrato l`, `triangolo a b c` (interi positivi).

## Uscita

`tipo perimetro`, oppure `triangolo non valido`, oppure `tipo sconosciuto: nome` per una forma che non conosci.

## Vincoli

Un'interfaccia `Forma`, `Quadrato` che estende `Rettangolo`, e il controllo nel costruttore del triangolo.

## Esempio

Ingresso:

```text
rettangolo 3 4
quadrato 5
triangolo 3 4 5
```

Uscita:

```text
rettangolo 14
quadrato 20
triangolo 12
```

## Come si lavora

1. `fauser nuovo E03 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

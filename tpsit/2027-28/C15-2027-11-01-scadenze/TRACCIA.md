# C15 · Scadenze

- **Materia:** TPSIT, anno scolastico 2027-28 · **L15** (slot 15 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-11-01) · slide: `materiali/tpsit5/p32/L15-chat-tcp/`
- **Compito della lezione 15**, per preparare la lezione 16 · Pool di thread, timeout, chiusura ordinata.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C15-2027-11-01-scadenze/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un server chiude i client **inattivi**. Ti arriva la lista dei messaggi con il tempo (in secondi) e il nome del client. Un messaggio è `scaduto` se dal messaggio precedente **dello stesso client** è passato **più di `T`** secondi; il primo messaggio di un client è sempre `ok`.

## Ingresso

Una riga con `T`, poi righe `tempo nome` con tempi non decrescenti.

## Uscita

Una riga per messaggio: `nome ok` oppure `nome scaduto`.

## Vincoli

Prepara la lezione 16: è l'idea del timeout.

## Esempio

Ingresso:

```text
10
0 a
5 a
20 a
```

Uscita:

```text
a ok
a ok
a scaduto
```

## Come si lavora

1. `fauser nuovo C15 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

# E26 · Chat: i messaggi privati

- **Materia:** TPSIT, anno scolastico 2027-28 · **L15** (slot 15 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-11-01) · slide: `materiali/tpsit5/p32/L15-chat-tcp/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E26-2027-11-01-chat-privato/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Aggiungi alla chat di E25 i **messaggi privati**: un testo che comincia con `@nome` va **solo** a quel destinatario. Se il destinatario non esiste (o è il mittente stesso) il mittente riceve un errore.

## Ingresso

Come E25. Un testo `@nome parole` è un messaggio privato.

## Uscita

Messaggio normale: `destinatario riceve mittente: testo` per gli altri client. Messaggio privato: `destinatario riceve mittente (privato): testo`. Destinatario sconosciuto: `mittente riceve ERR destinatario sconosciuto`.

## Vincoli

Il server distingue i due casi guardando il primo carattere del testo.

## Esempio

Ingresso:

```text
anna bruno carla
anna @bruno ciao
bruno tutti qui
```

Uscita:

```text
bruno riceve anna (privato): ciao
anna riceve bruno: tutti qui
carla riceve bruno: tutti qui
```

## Come si lavora

1. `fauser nuovo E26 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

# E09 - File binario ad accesso diretto

- **Livello:** sfida
- **Lezione:** Struct, tabelle e file: programma a menu carica/inserisci/salva (lun 30/11/2026)
- **Cartella della consegna:** `informatica/2026-27/esercizi/E09-2026-11-30-file-binario/`
- **Linguaggio:** quello scelto da te (`lang.txt`), uno degli otto ammessi.
- **Scadenza:** la fissa il docente in classe (giorno e ora).

## Cosa fare

Gestisci un **file binario di record** a lunghezza fissa. Ogni record è fatto da due interi a 32 bit: `codice` e `quantita` (8 byte in tutto, in formato little-endian). Il record numero `k` sta al byte `k * 8`: puoi leggerlo e cambiarlo **senza leggere gli altri** (accesso diretto).

## Regole

- Apri il file con `NUOVO` e poi lavora **sempre sul file**: ogni comando legge o scrive il file, non una copia in memoria di tutta la tabella.
- Per cambiare una quantità, **riscrivi solo i 4 byte** di quel campo (seek e scrittura sul posto).
- Interi a 32 bit con segno, little-endian (in Java `writeInt` è big-endian: per la traccia serve little-endian; vedi la nota del docente).

## Ingresso

Comandi, uno per riga, fino a `FINE`:
- `NUOVO file`: crea (o svuota) il file; è il primo comando di ogni prova.
- `A codice quantita`: aggiungi un record in fondo.
- `R k`: leggi il record `k` (da 0).
- `M k quantita`: cambia la quantità del record `k`.
- `N`: quanti record.
- `P`: stampa tutti i record.
- `FINE`: fine.

## Uscita

- `R`: `k: codice quantita`, oppure `Assente: k` se `k` non esiste (anche se negativo).
- `M`: `Modificato: k` oppure `Assente: k`.
- `N`: `Record: n`.
- `P`: una riga `k: codice quantita` per record, oppure `Vuoto`.
- `NUOVO` e `A`: niente.

## Esempio

Ingresso:

```text
NUOVO e09-01.bin
A 101 50
A 102 20
N
R 1
R 5
M 0 99
P
FINE
```

Uscita attesa:

```text
Record: 2
1: 102 20
Assente: 5
Modificato: 0
0: 101 99
1: 102 20
```

## Suggerimenti

- Il numero di record è `dimensione del file / 8`.
- Controlla `k` prima di fare il seek: un `k` troppo grande non deve fare errori.

## Come si controlla

- Il programma legge da **standard input** e scrive su **standard output**; niente messaggi del tipo «Inserisci...».
- Provalo con `fauser test`: usa i 3 casi pubblici di `tests/`. Il docente rifà girare anche altri casi che non vedi (valori limite, ingressi vuoti, numeri negativi): pensa ai casi particolari.
- Nel `README.md` scrivi come hai pensato la soluzione e come hai usato l'AI (se l'hai usata).

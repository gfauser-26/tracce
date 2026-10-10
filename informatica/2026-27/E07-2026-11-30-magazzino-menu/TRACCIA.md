# E07 - Magazzino a menu: modifica ed elimina

- **Livello:** intermedio
- **Lezione:** Struct, tabelle e file: programma a menu carica/inserisci/salva (lun 30/11/2026)
- **Cartella della consegna:** `informatica/2026-27/esercizi/E07-2026-11-30-magazzino-menu/`
- **Linguaggio:** quello scelto da te (`lang.txt`), uno degli otto ammessi.
- **Scadenza:** la fissa il docente in classe (giorno e ora).

## Cosa fare

Parti dal programma a menu visto a lezione (esempio `tabella-file`: inserisci, stampa, salva su file di testo, svuota, carica) e aggiungi tre comandi: **modifica la quantità**, **elimina un articolo** e **totale dei pezzi**.

## Regole

- Un articolo ha: `codice` (intero, unico), `nome` (una sola parola), `quantita` (intero).
- La tabella tiene l'ordine di inserimento; quando elimini, gli altri articoli restano nello stesso ordine.
- Il file di testo ha una riga per articolo: `codice;nome;quantita`.

## Ingresso

Comandi, uno per riga, fino a `Q`:
- `I codice nome quantita`: inserisci.
- `M codice quantita`: cambia la quantità.
- `X codice`: elimina l'articolo.
- `P`: stampa la tabella.
- `T`: totale dei pezzi.
- `S file`: salva sul file.
- `V`: svuota la tabella (non il file).
- `L file`: carica dal file, **sostituendo** la tabella.
- `Q`: fine.

## Uscita

- `I`: `Inserito: codice` oppure, se il codice c'è già (e non si inserisce), `Esiste: codice`.
- `M`: `Modificato: codice` oppure `Assente: codice`.
- `X`: `Eliminato: codice` oppure `Assente: codice`.
- `P`: una riga `codice nome quantita` per articolo, oppure `Tabella vuota`.
- `T`: `Totale pezzi: n`.
- `S`: `Salvati: n`.
- `V`: `Svuotata`.
- `L`: `Caricati: n`, oppure `File mancante` se il file non esiste (la tabella non cambia).

## Esempio

Ingresso:

```text
I 10 vite 5
I 20 dado 7
M 10 9
P
T
Q
```

Uscita attesa:

```text
Inserito: 10
Inserito: 20
Modificato: 10
10 vite 9
20 dado 7
Totale pezzi: 16
```

## Suggerimenti

- Eliminare da un vettore: sposta di una posizione indietro tutti gli articoli che seguono (o usa `Remove` / `del`).
- Prova il file con tabella vuota: `S` e poi `L` devono dare 0.

## Come si controlla

- Il programma legge da **standard input** e scrive su **standard output**; niente messaggi del tipo «Inserisci...».
- Provalo con `fauser test`: usa i 3 casi pubblici di `tests/`. Il docente rifà girare anche altri casi che non vedi (valori limite, ingressi vuoti, numeri negativi): pensa ai casi particolari.
- Nel `README.md` scrivi come hai pensato la soluzione e come hai usato l'AI (se l'hai usata).

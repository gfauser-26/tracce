# E08 - Carica un file con righe sbagliate

- **Livello:** intermedio
- **Lezione:** Struct, tabelle e file: programma a menu carica/inserisci/salva (lun 30/11/2026)
- **Cartella della consegna:** `informatica/2026-27/esercizi/E08-2026-11-30-carica-con-errori/`
- **Linguaggio:** quello scelto da te (`lang.txt`), uno degli otto ammessi.
- **Scadenza:** la fissa il docente in classe (giorno e ora).

## Cosa fare

Un file CSV vero ha quasi sempre qualche riga rovinata. Il programma riceve dallo standard input il **contenuto** di un file CSV (come se fosse il file), lo **scrive** in un file di testo `carica.csv`, lo **rilegge da quel file** e carica gli articoli, saltando le righe sbagliate senza fermarsi.

## Regole

- Una riga è **valida** se ha esattamente 3 campi separati da `;`, il primo (`codice`) e il terzo (`quantita`) sono numeri interi **senza segno e senza spazi** (solo cifre), e il secondo (`nome`) non è vuoto (può contenere spazi).
- Le righe completamente vuote non si scrivono nel file e non si contano.
- Le righe sbagliate si numerano a partire da 1, contando le righe scritte nel file (cioè senza le righe vuote).
- Non deve mai esserci un errore a runtime (niente eccezioni non gestite).

## Ingresso

- Righe di testo fino alla fine dell'ingresso (può essere vuoto).

## Uscita

- Per ogni riga sbagliata: `Riga i ignorata`.
- Poi tre righe: `Validi: v`, `Ignorate: e`, `Totale pezzi: t` (somma delle quantità delle righe valide).

## Esempio

Ingresso:

```text
101;vite;50
102;dado;20
```

Uscita attesa:

```text
Validi: 2
Ignorate: 0
Totale pezzi: 70
```

## Suggerimenti

- Dividi con `Split(';')` (C#), `split(";")` (Java, Python, TS), `strings.Split` (Go), `strtok` o `sscanf` (C).
- Fai prima il caso che funziona, poi un controllo alla volta: numero di campi, codice, nome, quantità.

## Come si controlla

- Il programma legge da **standard input** e scrive su **standard output**; niente messaggi del tipo «Inserisci...».
- Provalo con `fauser test`: usa i 3 casi pubblici di `tests/`. Il docente rifà girare anche altri casi che non vedi (valori limite, ingressi vuoti, numeri negativi): pensa ai casi particolari.
- Nel `README.md` scrivi come hai pensato la soluzione e come hai usato l'AI (se l'hai usata).

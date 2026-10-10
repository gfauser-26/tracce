# E10 - Dizionario con vettore dinamico

- **Livello:** sfida
- **Lezione:** Dizionario: stringhe, file e vettori dinamici (sfida del compito di lun 30/11/2026)
- **Cartella della consegna:** `informatica/2026-27/esercizi/E10-2026-11-30-dizionario-dinamico/`
- **Linguaggio:** quello scelto da te (`lang.txt`), uno degli otto ammessi.
- **Scadenza:** la fissa il docente in classe (giorno e ora).

## Cosa fare

Parti dall'esempio `dizionario` della lezione e costruisci un dizionario inglese-italiano che si può modificare: aggiungere, tradurre, eliminare, salvare e ricaricare. Le voci stanno in un **vettore dinamico** (in C: `realloc` e `free`, comprese le stringhe copiate con `strdup`).

## Regole

- Una voce è una coppia `en it` (due parole). Il confronto tra le parole inglesi **non distingue maiuscole e minuscole**.
- Se aggiungi una voce con `en` già presente, **sostituisci la traduzione** e tieni la scrittura di `en` che c'era.
- Il file ha una riga per voce: `en;it`.
- Niente ordinamento e niente ricerca binaria: cerca scorrendo il vettore.

## Ingresso

Comandi, uno per riga, fino a `Q`:
- `A en it`: aggiungi (o aggiorna).
- `T en`: traduci.
- `D en`: elimina.
- `N`: quante voci.
- `S file`: salva.
- `L file`: carica, sostituendo le voci.
- `Q`: fine.

## Uscita

- `A`: `Aggiunta: en` oppure `Aggiornata: en` (con `en` come scritto nel comando).
- `T`: `en -> it`, oppure `en -> ?` (con `en` come scritto nel comando).
- `D`: `Eliminata: en` oppure `Assente: en`.
- `N`: `Voci: n`.
- `S`: `Salvate: n`.
- `L`: `Caricate: n`, oppure `File mancante`.

## Esempio

Ingresso:

```text
A dog cane
A cat gatto
T Dog
T bird
N
Q
```

Uscita attesa:

```text
Aggiunta: dog
Aggiunta: cat
Dog -> cane
bird -> ?
Voci: 2
```

## Suggerimenti

- Eliminare dal vettore: sposta indietro le voci successive. In C ricordati di fare `free` delle due stringhe della voce eliminata.
- Pensa ai casi: dizionario vuoto, file vuoto, ultima voce eliminata.

## Come si controlla

- Il programma legge da **standard input** e scrive su **standard output**; niente messaggi del tipo «Inserisci...».
- Provalo con `fauser test`: usa i 3 casi pubblici di `tests/`. Il docente rifà girare anche altri casi che non vedi (valori limite, ingressi vuoti, numeri negativi): pensa ai casi particolari.
- Nel `README.md` scrivi come hai pensato la soluzione e come hai usato l'AI (se l'hai usata).

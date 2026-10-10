# E11 - Quante volte compare ogni parola

- **Livello:** intermedio
- **Lezione:** Dizionario: stringhe, file e vettori dinamici (sfida del compito di lun 30/11/2026)
- **Cartella della consegna:** `informatica/2026-27/esercizi/E11-2026-11-30-frequenza-parole/`
- **Linguaggio:** quello scelto da te (`lang.txt`), uno degli otto ammessi.
- **Scadenza:** la fissa il docente in classe (giorno e ora).

## Cosa fare

Leggi un testo e conta quante volte compare ogni parola. È un dizionario in cui il valore è un numero: parola e contatore. Le parole nuove si aggiungono man mano.

## Regole

- Una **parola** è una sequenza di lettere dell'alfabeto inglese (`a-z`, `A-Z`). Tutto il resto (spazi, punteggiatura, cifre, apostrofi, trattini) separa le parole: `l'albero` sono due parole, `l` e `albero`.
- Maiuscole e minuscole sono uguali: si stampa in minuscolo.
- Niente ordinamento: le parole si stampano **nell'ordine in cui compaiono la prima volta**.

## Ingresso

- Un testo di una o più righe, fino alla fine dell'ingresso (può essere vuoto).

## Uscita

- Per ogni parola distinta: `parola: n`.
- Poi `Parole: t` (totale delle parole lette) e `Distinte: d`.

## Esempio

Ingresso:

```text
Il gatto e il cane.
Il cane dorme!
```

Uscita attesa:

```text
il: 3
gatto: 1
e: 1
cane: 2
dorme: 1
Parole: 8
Distinte: 5
```

## Suggerimenti

- In C#, Java, Python, Go, TS puoi usare un dizionario (`Dictionary`, `HashMap`, `dict`, `map`) ma devi ricordare l'ordine di arrivo: conserva anche un elenco delle parole. In C usa un vettore di struct con parola e contatore.
- Scrivi prima un programma che separa le parole e le stampa una per riga: poi aggiungi il conteggio.

## Come si controlla

- Il programma legge da **standard input** e scrive su **standard output**; niente messaggi del tipo «Inserisci...».
- Provalo con `fauser test`: usa i 3 casi pubblici di `tests/`. Il docente rifà girare anche altri casi che non vedi (valori limite, ingressi vuoti, numeri negativi): pensa ai casi particolari.
- Nel `README.md` scrivi come hai pensato la soluzione e come hai usato l'AI (se l'hai usata).

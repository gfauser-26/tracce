# E03 - Stipendi di un'azienda

- **Livello:** intermedio
- **Lezione:** Classi ed ereditarietà: portamonete e portafoglio (ven 23/10/2026)
- **Cartella della consegna:** `informatica/2026-27/esercizi/E03-2026-10-23-stipendi/`
- **Linguaggio:** quello scelto da te (`lang.txt`), uno degli otto ammessi.
- **Scadenza:** la fissa il docente in classe (giorno e ora).

## Cosa fare

Una classe base `Dipendente` ha lo stipendio base. Tre classi derivate calcolano lo stipendio in modo diverso. Scrivi le classi e un programma che legge i dipendenti e stampa quanto costano.

## Regole

- `Impiegato` (`I base`): stipendio = `base`.
- `Dirigente` (`D base`): stipendio = `base` più il 10% di `base`, con la **divisione intera** (`base / 10`, senza decimali).
- `Operaio` (`O base ore tariffa`): stipendio = `base + ore * tariffa`.
- Tutti i numeri sono interi.

## Ingresso

- Riga 1: `n`, il numero di dipendenti.
- Poi `n` righe nei formati sopra.

## Uscita

- Per ogni dipendente, una riga `Nome: stipendio`, con `Nome` uguale a `Impiegato`, `Dirigente` o `Operaio`.
- Una riga `Costo totale: s`.

## Esempio

Ingresso:

```text
3
I 1000
D 2000
O 800 10 15
```

Uscita attesa:

```text
Impiegato: 1000
Dirigente: 2200
Operaio: 950
Costo totale: 4150
```

## Suggerimenti

- Quale metodo ridefinisce ogni classe derivata? Quale resta uguale?
- Occhio al `Dirigente` con base 5: il 10% è 0, non 0,5.

## Come si controlla

- Il programma legge da **standard input** e scrive su **standard output**; niente messaggi del tipo «Inserisci...».
- Provalo con `fauser test`: usa i 3 casi pubblici di `tests/`. Il docente rifà girare anche altri casi che non vedi (valori limite, ingressi vuoti, numeri negativi): pensa ai casi particolari.
- Nel `README.md` scrivi come hai pensato la soluzione e come hai usato l'AI (se l'hai usata).

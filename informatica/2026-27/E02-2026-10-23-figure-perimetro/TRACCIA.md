# E02 - Figure e perimetri

- **Livello:** base
- **Lezione:** Classi ed ereditarietà: portamonete e portafoglio (ven 23/10/2026)
- **Cartella della consegna:** `informatica/2026-27/esercizi/E02-2026-10-23-figure-perimetro/`
- **Linguaggio:** quello scelto da te (`lang.txt`), uno degli otto ammessi.
- **Scadenza:** la fissa il docente in classe (giorno e ora).

## Cosa fare

Scrivi una classe base `Figura` con il metodo `Perimetro()` e tre classi: `Rettangolo`, `Quadrato` e `Triangolo` (equilatero). Il `Quadrato` **eredita dal `Rettangolo`**: il suo costruttore chiama quello della classe base con lo stesso lato due volte.

## Regole

- Rettangolo di lati `a` e `b`: perimetro `2 * (a + b)`.
- Quadrato di lato `l`: è un rettangolo con `a = b = l`.
- Triangolo equilatero di lato `l`: perimetro `3 * l`.
- Tutti i numeri sono interi.

## Ingresso

- Riga 1: `n`, il numero di figure.
- Poi `n` righe: `R a b`, oppure `Q l`, oppure `T l`.

## Uscita

- Per ogni figura, una riga `Nome: perimetro`, con `Nome` uguale a `Rettangolo`, `Quadrato` o `Triangolo`.
- Una riga `Somma: s`, con la somma dei perimetri.
- Una riga `Maggiore: Nome`, con il nome della figura di perimetro maggiore (a parità, la prima); se non ci sono figure, `Maggiore: nessuna`.

## Esempio

Ingresso:

```text
3
R 3 4
Q 5
T 2
```

Uscita attesa:

```text
Rettangolo: 14
Quadrato: 20
Triangolo: 6
Somma: 40
Maggiore: Quadrato
```

## Suggerimenti

- Il nome stampato per un quadrato è `Quadrato`, anche se è anche un rettangolo: ogni classe sa il proprio nome.
- Per il maggiore: scorri una volta sola e ricorda la migliore finora, senza ordinare.

## Come si controlla

- Il programma legge da **standard input** e scrive su **standard output**; niente messaggi del tipo «Inserisci...».
- Provalo con `fauser test`: usa i 3 casi pubblici di `tests/`. Il docente rifà girare anche altri casi che non vedi (valori limite, ingressi vuoti, numeri negativi): pensa ai casi particolari.
- Nel `README.md` scrivi come hai pensato la soluzione e come hai usato l'AI (se l'hai usata).

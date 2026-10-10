# E01 - Conti correnti: la regola del prelievo cambia

- **Livello:** intermedio
- **Lezione:** Classi ed ereditarietà: portamonete e portafoglio (ven 23/10/2026)
- **Cartella della consegna:** `informatica/2026-27/esercizi/E01-2026-10-23-conti-correnti/`
- **Linguaggio:** quello scelto da te (`lang.txt`), uno degli otto ammessi.
- **Scadenza:** la fissa il docente in classe (giorno e ora).

## Cosa fare

Scrivi una classe base `Conto` e una classe derivata `ContoFido`. Il **prelievo** segue una regola diversa nei due casi: è il metodo che la classe derivata ridefinisce (override). Il resto del programma deve trattare tutti i conti allo stesso modo.

## Regole

- `Conto` (tipo `S`): si può prelevare un importo solo se è maggiore di 0 e **non supera il saldo**.
- `ContoFido` (tipo `F`): si può prelevare se l'importo è maggiore di 0 e il saldo dopo il prelievo **non scende sotto `-fido`** (il saldo può diventare negativo, fino al fido).
- Versamento: ammesso solo se l'importo è maggiore di 0, in tutti i conti.
- Importi e saldi sono interi (euro).

## Ingresso

- Riga 1: `n`, il numero di conti.
- Poi `n` righe: `S saldo` per un conto standard, `F saldo fido` per un conto con fido.
- Poi una riga con `m`, il numero di operazioni.
- Poi `m` righe: `V i importo` (versa) oppure `P i importo` (preleva), dove `i` è l'indice del conto (da 0).

## Uscita

- Per ogni operazione, una riga: `ok` oppure `rifiutato`.
- Alla fine, per ogni conto, una riga `Conto i: saldo`.

## Esempio

Ingresso:

```text
2
S 100
F 50 100
4
P 0 30
P 0 100
P 1 120
V 1 10
```

Uscita attesa:

```text
ok
rifiutato
ok
ok
Conto 0: 70
Conto 1: -60
```

## Suggerimenti

- Disegna prima l'UML: `ContoFido` che cosa aggiunge? Che cosa ridefinisce?
- Metti i conti in un vettore (o lista) del tipo della classe base e chiama sempre lo stesso metodo: è il polimorfismo.
- In C: una `struct` con un puntatore a funzione, come nell'esempio `portamonete` della lezione.

## Come si controlla

- Il programma legge da **standard input** e scrive su **standard output**; niente messaggi del tipo «Inserisci...».
- Provalo con `fauser test`: usa i 3 casi pubblici di `tests/`. Il docente rifà girare anche altri casi che non vedi (valori limite, ingressi vuoti, numeri negativi): pensa ai casi particolari.
- Nel `README.md` scrivi come hai pensato la soluzione e come hai usato l'AI (se l'hai usata).

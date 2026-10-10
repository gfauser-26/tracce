# E13 · Endpoint validi e tipo di porta

- **Materia:** TPSIT, anno scolastico 2027-28 · **L09** (slot 9 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-11) · slide: `materiali/tpsit5/p32/L09-client-server-e-socket/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E13-2027-10-11-endpoint/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un **endpoint** è `indirizzo:porta`. È valido se l'indirizzo IPv4 ha quattro numeri da 0 a 255 separati da punti e la porta va da 1 a 65535. Se è valido, di' di che tipo è la porta: `nota` (1-1023), `registrata` (1024-49151), `dinamica` (49152-65535).

## Ingresso

Un endpoint per riga, come testo.

## Uscita

`endpoint valido tipo` oppure `endpoint non valido`.

## Vincoli

Spezza il testo con i due punti e con i punti; controlla che siano numeri prima di convertirli.

## Esempio

Ingresso:

```text
127.0.0.1:80
192.168.1.10:5000
10.0.0.1:50000
```

Uscita:

```text
127.0.0.1:80 valido nota
192.168.1.10:5000 valido registrata
10.0.0.1:50000 valido dinamica
```

## Come si lavora

1. `fauser nuovo E13 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

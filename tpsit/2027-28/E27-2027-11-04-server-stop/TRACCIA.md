# E27 · Server che si ferma con STOP

- **Materia:** TPSIT, anno scolastico 2027-28 · **L16** (slot 16 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-11-04) · slide: `materiali/tpsit5/p32/L16-pool-timeout-collaudo/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E27-2027-11-04-server-stop/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un server TCP (socket veri su `127.0.0.1`, porta 0) risponde ai comandi `PING` (con `PONG`) e `ECHO testo` (con il testo); ogni altro comando riceve `ERR`. Il comando `STOP` risponde `ARRESTO` e **ferma il server in modo ordinato**: niente nuove connessioni, il lavoro in corso finisce. Le righe dopo `STOP` non vengono inviate. Alla fine il programma stampa quante richieste (escluso `STOP`) ha servito.

## Ingresso

Un comando per riga.

## Uscita

Una risposta per comando, poi `servite N`.

## Vincoli

Chiudi il `ServerSocket`, poi attendi la fine dei thread o del pool (`shutdown` e `awaitTermination`).

## Esempio

Ingresso:

```text
PING
ECHO ciao a tutti
STOP
PING
```

Uscita:

```text
PONG
ciao a tutti
ARRESTO
servite 2
```

## Come si lavora

1. `fauser nuovo E27 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

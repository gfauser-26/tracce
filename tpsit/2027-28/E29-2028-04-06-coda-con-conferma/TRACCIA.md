# E29 · Coda con conferma e riconsegna

- **Materia:** TPSIT, anno scolastico 2027-28 · **L50** (slot 50 del programma `programmazione/TPSIT5.md`, data ipotetica 2028-04-06) · slide: `materiali/tpsit5/p32/L50-broker-e-code-di-messaggi/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E29-2028-04-06-coda-con-conferma/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Simula una **coda di messaggi** con conferma (come RabbitMQ), in memoria. I messaggi hanno un identificativo crescente da 1. Un messaggio consegnato (`GET`) resta «in corso» finché non è confermato (`ACK`); con `NACK` torna **in testa** alla coda per essere riconsegnato.

## Ingresso

Un comando per riga: `PUB testo` (il testo può avere spazi), `GET`, `ACK id`, `NACK id`, `STATO`.

## Uscita

`PUB` → `OK id`; `GET` → `MSG id testo` oppure `VUOTA`; `ACK`/`NACK` → `OK` oppure `ERR sconosciuto` (id non in corso); `STATO` → `pronti P in corso C`; comando che non esiste → `ERR comando sconosciuto`.

## Vincoli

Una lista per i messaggi pronti e una mappa per quelli in corso. Nessun socket.

## Esempio

Ingresso:

```text
PUB uno
PUB due
GET
ACK 1
STATO
```

Uscita:

```text
OK 1
OK 2
MSG 1 uno
OK
pronti 1 in corso 0
```

## Come si lavora

1. `fauser nuovo E29 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

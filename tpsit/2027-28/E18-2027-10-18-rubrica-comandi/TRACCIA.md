# E18 · Rubrica a comandi

- **Materia:** TPSIT, anno scolastico 2027-28 · **L11** (slot 11 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-18) · slide: `materiali/tpsit5/p32/L11-protocollo-a-comandi/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E18-2027-10-18-rubrica-comandi/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un server TCP tiene una **rubrica** chiave → valore (client e server nello stesso programma, `127.0.0.1`, porta 0). Comandi: `SET chiave valore`, `GET chiave`, `DEL chiave`, `COUNT`. Chiavi e valori sono una parola.

## Ingresso

Un comando per riga.

## Uscita

`SET` → `OK`; `GET` → `VALORE v` oppure `ERR assente`; `DEL` → `OK` oppure `ERR assente`; `COUNT` → `NUMERO n`; numero di argomenti sbagliato → `ERR argomenti`; comando che non esiste → `ERR comando sconosciuto`.

## Vincoli

Una mappa nel server. Con più client servirebbe un lucchetto (lezione 12): per ora un solo client.

## Esempio

Ingresso:

```text
SET a 1
GET a
COUNT
```

Uscita:

```text
OK
VALORE 1
NUMERO 1
```

## Come si lavora

1. `fauser nuovo E18 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

# C14 · Elenco dei collegati

- **Materia:** TPSIT, anno scolastico 2027-28 · **L14** (slot 14 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-28) · slide: `materiali/tpsit5/p32/L14-byte-oggetti-protocollo/`
- **Compito della lezione 14**, per preparare la lezione 15 · Chat TCP a console.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C14-2027-10-28-elenco-collegati/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Tieni l'elenco dei nomi collegati a una chat. Comandi: `ENTRA nome`, `ESCE nome`, `CHI`.

## Ingresso

Un comando per riga.

## Uscita

`ENTRA` → `OK` oppure `ERR nome già usato`; `ESCE` → `OK` oppure `ERR sconosciuto`; `CHI` → `collegati: n1 n2 ...` (in ordine di ingresso) oppure `nessuno`.

## Vincoli

Prepara la lezione 15: l'elenco sarà condiviso tra più thread.

## Esempio

Ingresso:

```text
ENTRA anna
ENTRA bruno
CHI
```

Uscita:

```text
OK
OK
collegati: anna bruno
```

## Come si lavora

1. `fauser nuovo C14 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

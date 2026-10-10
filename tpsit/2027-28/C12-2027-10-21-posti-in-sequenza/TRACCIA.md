# C12 · Posti in sequenza

- **Materia:** TPSIT, anno scolastico 2027-28 · **L12** (slot 12 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-21) · slide: `materiali/tpsit5/p32/L12-server-multithread/`
- **Compito della lezione 12**, per preparare la lezione 13 · Crociera: biglietti con posti limitati.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C12-2027-10-21-posti-in-sequenza/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Ci sono `P` posti. Arrivano dei client **uno dopo l'altro** (senza concorrenza); ognuno chiede un certo numero di biglietti, **tutti o nessuno**. Se i posti bastano, la richiesta è `OK` e i posti calano; altrimenti `COMPLETO`.

## Ingresso

Una riga con `P`, poi le richieste (interi positivi, anche su più righe).

## Uscita

`cliente i OK` o `cliente i COMPLETO` per ogni richiesta, poi `posti rimasti P`.

## Vincoli

Prepara la lezione 13: nella versione concorrente il controllo e la vendita non si potranno separare.

## Esempio

Ingresso:

```text
5
2 2 2
```

Uscita:

```text
cliente 1 OK
cliente 2 OK
cliente 3 COMPLETO
posti rimasti 1
```

## Come si lavora

1. `fauser nuovo C12 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

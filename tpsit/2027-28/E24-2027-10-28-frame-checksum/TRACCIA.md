# E24 · Messaggio con checksum

- **Materia:** TPSIT, anno scolastico 2027-28 · **L14** (slot 14 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-28) · slide: `materiali/tpsit5/p32/L14-byte-oggetti-protocollo/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E24-2027-10-28-frame-checksum/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un messaggio ha **4 byte di lunghezza** (big-endian), il **testo**, e in coda **1 byte di checksum**, lo XOR di tutti i byte del testo. Per ogni messaggio ricevuto (scritto in esadecimale) di' se è valido.

## Ingresso

Un messaggio per riga: byte in esadecimale separati da spazio.

## Uscita

`valido testo` se lunghezza e checksum sono giusti; `errore lunghezza` se i byte non sono `4 + lunghezza + 1`; altrimenti `errore checksum`. Si controlla prima la lunghezza.

## Vincoli

Converti ogni coppia di cifre in un byte. Lo XOR si calcola con l'operatore `^`.

## Esempio

Ingresso:

```text
00 00 00 04 63 69 61 6f 04
00 00 00 01 61 00
```

Uscita:

```text
valido ciao
errore checksum
```

## Come si lavora

1. `fauser nuovo E24 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

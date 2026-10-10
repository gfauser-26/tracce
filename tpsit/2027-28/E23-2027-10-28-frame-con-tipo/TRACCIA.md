# E23 · Messaggio con tipo e lunghezza

- **Materia:** TPSIT, anno scolastico 2027-28 · **L14** (slot 14 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-28) · slide: `materiali/tpsit5/p32/L14-byte-oggetti-protocollo/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E23-2027-10-28-frame-con-tipo/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Costruisci un messaggio (frame): **1 byte di tipo**, poi **4 byte di lunghezza** in big-endian, poi il testo in UTF-8. Per ogni riga di ingresso stampa i byte del frame in esadecimale, poi ricostruisci tipo e testo leggendo il frame.

## Ingresso

Righe `tipo testo`, con `tipo` intero da 0 a 255 e testo ASCII (può contenere spazi).

## Uscita

Per ogni riga due righe: i byte in esadecimale minuscolo separati da spazio, poi `tipo T: testo`.

## Vincoli

La lunghezza è in **byte**, non in caratteri. Non fidarti dell'ordine dei byte della tua macchina: scrivili tu uno per uno o usa le funzioni big-endian.

## Esempio

Ingresso:

```text
1 ciao
```

Uscita:

```text
01 00 00 00 04 63 69 61 6f
tipo 1: ciao
```

## Come si lavora

1. `fauser nuovo E23 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

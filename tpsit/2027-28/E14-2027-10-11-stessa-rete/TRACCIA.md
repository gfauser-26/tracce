# E14 · Stessa rete o no?

- **Materia:** TPSIT, anno scolastico 2027-28 · **L09** (slot 9 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-11) · slide: `materiali/tpsit5/p32/L09-client-server-e-socket/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E14-2027-10-11-stessa-rete/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Due computer sono nella **stessa rete** se i loro indirizzi coincidono nei primi `p` bit (il prefisso, come in `/24`). Dati due indirizzi IPv4 e il prefisso, dì se sono nella stessa rete.

## Ingresso

Una riga per caso: `indirizzo1 indirizzo2 prefisso` (prefisso da 1 a 32). Gli indirizzi sono validi.

## Uscita

`stessa rete` oppure `reti diverse`.

## Vincoli

Trasforma l'indirizzo in un intero a 32 bit (un byte ogni 8 bit), costruisci la maschera con `p` bit a 1 e fai l'AND. Attenzione ai tipi: in Java usa `long` o interi senza segno.

## Esempio

Ingresso:

```text
192.168.1.10 192.168.1.200 24
10.0.0.1 10.0.1.1 24
```

Uscita:

```text
stessa rete
reti diverse
```

## Come si lavora

1. `fauser nuovo E14 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

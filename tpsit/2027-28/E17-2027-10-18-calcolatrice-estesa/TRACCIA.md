# E17 · Calcolatrice con potenze e resto

- **Materia:** TPSIT, anno scolastico 2027-28 · **L11** (slot 11 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-18) · slide: `materiali/tpsit5/p32/L11-protocollo-a-comandi/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E17-2027-10-18-calcolatrice-estesa/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Estendi la calcolatrice online (client e server TCP nello stesso programma, `127.0.0.1`, porta 0) con i comandi `POW a b` (potenza) e `MOD a b` (resto). Il server deve rispondere `ERR argomenti` anche quando un argomento **non è un numero intero**, senza cadere.

## Ingresso

Una richiesta per riga: `ADD`, `SUB`, `MUL`, `DIV`, `POW`, `MOD` con due interi. Per `MOD` e `POW` gli argomenti validi sono `a ≥ 0` e `b ≥ 0`.

## Uscita

`OK risultato`, oppure `ERR comando sconosciuto`, `ERR argomenti`, `ERR divisione per zero` (anche per `MOD` con `b = 0`), `ERR esponente` (`POW` con `b < 0`). I controlli si fanno **in questo ordine**: comando, numero di argomenti, argomenti interi, poi divisione per zero ed esponente.

## Vincoli

`DIV` è la divisione intera. Tieni la funzione `rispondi(riga)` separata dai socket, come nell'esempio.

## Esempio

Ingresso:

```text
POW 2 10
MOD 17 5
ADD 1 2
```

Uscita:

```text
OK 1024
OK 2
OK 3
```

## Come si lavora

1. `fauser nuovo E17 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

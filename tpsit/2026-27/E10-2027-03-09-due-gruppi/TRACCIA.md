# E10 · Due gruppi nella stessa stanza

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA5 Comunicazione e sincronizzazione**
- **Lezione:** 4BIN n. 39 (mar 09/03), 4DIN n. 22 (lun 05/04) · slide: `materiali/tpsit4/p32/applicazioni-semafori/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E10-2027-03-09-due-gruppi/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Una stanza e due gruppi di thread: `a` thread del **gruppo 1** e `b` del **gruppo 2**. Ogni thread entra `c` volte, resta 1 ms e esce. Nella stanza possono stare **tanti thread dello stesso gruppo insieme**, ma **mai uno di un gruppo con uno dell'altro**. Usa lo schema «il primo chiude la porta, l'ultimo la riapre» con i semafori.

Dentro la stanza controlla (con un contatore per gruppo, protetto) che non ci siano insieme thread dei due gruppi: se succede, aggiungi 1 alle **violazioni**.

## Ingresso

Una riga: `a b c`.

## Uscita

Tre righe: `ingressi gruppo 1: X`, `ingressi gruppo 2: Y`, `violazioni: V` (X = a * c, Y = b * c, V = 0).

## Vincoli

1 <= a, b <= 8; 1 <= c <= 20.

## Esempio

Ingresso:

```text
2 2 3
```

Uscita:

```text
ingressi gruppo 1: 6
ingressi gruppo 2: 6
violazioni: 0
```

## Come si lavora

1. `fauser nuovo E10 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

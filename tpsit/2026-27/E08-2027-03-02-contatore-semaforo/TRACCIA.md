# E08 · Contatore con semaforo binario

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA5 Comunicazione e sincronizzazione**
- **Lezione:** 4BIN n. 37 (mar 02/03), 4DIN n. 21 (lun 22/03) · slide: `materiali/tpsit4/p32/interleaving-lock/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E08-2027-03-02-contatore-semaforo/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Come il contatore della lezione, ma al posto del lock usa un **semaforo binario** (valore iniziale 1; `P` per entrare, `V` per uscire). `k` thread incrementano `m` volte un contatore condiviso.

## Ingresso

Una riga: `k m`.

## Uscita

Due righe: `contatore: C` e `atteso: A` (A = k * m).

## Vincoli

1 <= k <= 16; 1 <= m <= 100000. Il semaforo deve avere valore iniziale 1.

## Esempio

Ingresso:

```text
4 1000
```

Uscita:

```text
contatore: 4000
atteso: 4000
```

## Come si lavora

1. `fauser nuovo E08 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

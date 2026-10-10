# E09 · Rendez-vous a due

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA5 Comunicazione e sincronizzazione**
- **Lezione:** 4BIN n. 39 (mar 09/03), 4DIN n. 22 (lun 05/04) · slide: `materiali/tpsit4/p32/applicazioni-semafori/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E09-2027-03-09-rendez-vous/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Due thread, **A** e **B**, ripetono `R` round. In ogni round: **fase 1**, poi **rendez-vous** (ognuno aspetta l'altro, con **due semafori** a 0), poi **fase 2**.

Conta le fasi 1 completate da ciascun thread in un contatore suo. Nella fase 2 del round `r`, ogni thread controlla che **l'altro** abbia già finito la fase 1 del round `r` (contatore >= `r`): se no, aggiunge 1 alle **violazioni**.

## Ingresso

Una riga: `R`.

## Uscita

Due righe: `round completati: R` e `violazioni: V` (V deve essere 0 con i semafori giusti).

## Vincoli

1 <= R <= 5000. Niente attese attive: usa i semafori. Il docente legge il codice per controllare che ci siano davvero.

## Esempio

Ingresso:

```text
1
```

Uscita:

```text
round completati: 1
violazioni: 0
```

## Come si lavora

1. `fauser nuovo E09 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

## Nota

Se togli i semafori, le violazioni non sono sempre diverse da 0: per questo conta anche il codice.

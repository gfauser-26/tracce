# E06 · Classifica per punteggio

- **Materia:** TPSIT, anno scolastico 2027-28 · **L03** (slot 3 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-20) · slide: `materiali/tpsit5/p32/L03-collezioni-e-generics/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E06-2027-09-20-classifica/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Ogni riga assegna dei punti a una squadra. Somma i punti per squadra e stampa la classifica, dal punteggio **più alto**; a parità, in **ordine alfabetico**.

## Ingresso

Righe `squadra punti` (nome di una parola, punti interi non negativi).

## Uscita

Una riga per squadra: `squadra totale`.

## Vincoli

Una mappa nome → totale e un ordinamento con due criteri (comparatore).

## Esempio

Ingresso:

```text
rossa 3
blu 5
rossa 4
```

Uscita:

```text
rossa 7
blu 5
```

## Come si lavora

1. `fauser nuovo E06 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

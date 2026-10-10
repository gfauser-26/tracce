# C01 · Versi degli animali

- **Materia:** TPSIT, anno scolastico 2027-28 · **L01** (slot 1 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-13) · slide: `materiali/tpsit5/p32/L01-dal-csharp-a-java/`
- **Compito della lezione 01**, per preparare la lezione 02 · OOP in Java: ereditarietà, interfacce, eccezioni.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C01-2027-09-13-versi-animali/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Una classe base `Animale` ha il metodo `verso()`. Le classi `Cane` (`bau`), `Gatto` (`miao`) e `Mucca` (`muu`) la **estendono** e ridefiniscono il metodo. Il programma legge il tipo di animale e stampa il suo verso.

## Ingresso

Un tipo per riga (`cane`, `gatto`, `mucca` o altro).

## Uscita

Il verso, oppure `tipo sconosciuto: nome`.

## Vincoli

Prepara la lezione 2: guarda come si scrive `extends` e come si ridefinisce un metodo.

## Esempio

Ingresso:

```text
cane
gatto
```

Uscita:

```text
bau
miao
```

## Come si lavora

1. `fauser nuovo C01 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

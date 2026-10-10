# C05 · Un pool simulato

- **Materia:** TPSIT, anno scolastico 2027-28 · **L05** (slot 5 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-27) · slide: `materiali/tpsit5/p32/L05-thread-in-java/`
- **Compito della lezione 05**, per preparare la lezione 06 · Executor, lock e semafori.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C05-2027-09-27-pool-simulato/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Hai `W` lavoratori e `N` compiti, ciascuno con una durata. I compiti, **nell'ordine di ingresso**, vanno al lavoratore che si libera per primo (a parità, quello con il numero più basso). Tutti partono al tempo 0. Calcola il tempo di fine di ogni compito. Il tempo è **simulato**: niente thread.

## Ingresso

Una riga con `W N`, poi le `N` durate (interi positivi).

## Uscita

`compito i fine t` per ogni compito (i da 1), poi `fine totale T`.

## Vincoli

Prepara la lezione 6: è il comportamento di un pool di thread.

## Esempio

Ingresso:

```text
2 4
3 2 2 1
```

Uscita:

```text
compito 1 fine 3
compito 2 fine 2
compito 3 fine 4
compito 4 fine 4
fine totale 4
```

## Come si lavora

1. `fauser nuovo C05 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

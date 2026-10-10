# E01 · Conto con fido

- **Materia:** TPSIT, anno scolastico 2027-28 · **L01** (slot 1 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-13) · slide: `materiali/tpsit5/p32/L01-dal-csharp-a-java/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E01-2027-09-13-conto-con-fido/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Estendi il conto corrente della lezione: oltre ai comandi `versa`, `preleva` e `saldo`, il conto accetta il comando `fido N`, che imposta quanto si può andare **sotto zero**. Il fido iniziale è 0. Un prelievo che porterebbe il saldo sotto `-fido` è rifiutato e non cambia nulla.

## Ingresso

Un comando per riga: `fido N`, `versa N`, `preleva N`, `saldo`. Numeri interi non negativi.

## Uscita

`saldo X` per ogni comando `saldo` (X può essere negativo); `rifiutato` per ogni prelievo rifiutato.

## Vincoli

Usa una classe `Conto` con il campo `saldo` e il campo `fido` privati. Chi legge il programma deve vedere che nessun altro tocca il saldo.

## Esempio

Ingresso:

```text
fido 50
versa 20
preleva 60
saldo
```

Uscita:

```text
saldo -40
```

## Come si lavora

1. `fauser nuovo E01 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

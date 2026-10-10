# C02 · Frequenza delle lettere

- **Materia:** TPSIT, anno scolastico 2027-28 · **L02** (slot 2 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-16) · slide: `materiali/tpsit5/p32/L02-oop-in-java/`
- **Compito della lezione 02**, per preparare la lezione 03 · Collezioni e generics.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C02-2027-09-16-frequenza-lettere/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Conta quante volte compare ogni lettera dell'alfabeto inglese (`a`-`z`, maiuscole e minuscole uguali) nel testo. Ignora tutto il resto.

## Ingresso

Testo libero su più righe.

## Uscita

Una riga per ogni lettera che compare, in ordine alfabetico: `lettera conteggio`.

## Vincoli

Prepara la lezione 3: chiediti quale struttura ti serve per associare una lettera a un numero.

## Esempio

Ingresso:

```text
ciao
```

Uscita:

```text
a 1
c 1
i 1
o 1
```

## Come si lavora

1. `fauser nuovo C02 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

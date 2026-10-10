# C16 · Indirizzo di broadcast

- **Materia:** TPSIT, anno scolastico 2027-28 · **L16** (slot 16 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-11-04) · slide: `materiali/tpsit5/p32/L16-pool-timeout-collaudo/`
- **Compito della lezione 16**, per preparare la lezione 19 · UDP, datagrammi, scoperta di host.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C16-2027-11-04-indirizzo-broadcast/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

L'indirizzo di **broadcast** di una rete ha a 1 tutti i bit dopo il prefisso. Dato `indirizzo/prefisso` stampa l'indirizzo di broadcast.

## Ingresso

Un valore `a.b.c.d/p` per riga o separato da spazi (p da 1 a 31).

## Uscita

Un indirizzo per ogni valore.

## Vincoli

Prepara la lezione 19: il broadcast serve a trovare gli altri computer della rete.

## Esempio

Ingresso:

```text
192.168.1.10/24
```

Uscita:

```text
192.168.1.255
```

## Come si lavora

1. `fauser nuovo C16 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

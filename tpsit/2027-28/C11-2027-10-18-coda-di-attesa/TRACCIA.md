# C11 · Coda di attesa

- **Materia:** TPSIT, anno scolastico 2027-28 · **L11** (slot 11 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-10-18) · slide: `materiali/tpsit5/p32/L11-protocollo-a-comandi/`
- **Compito della lezione 11**, per preparare la lezione 12 · Server multithread.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C11-2027-10-18-coda-di-attesa/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un server **sequenziale** serve un client alla volta. Arrivano `N` client **tutti insieme** al tempo 0, ciascuno con un tempo di servizio. Calcola quanto aspetta ognuno prima di essere servito, nell'ordine di arrivo.

## Ingresso

Una riga con `N`, poi le `N` durate.

## Uscita

`cliente i attesa t` per ogni client (i da 1), poi `attesa totale T`.

## Vincoli

Prepara la lezione 12: capirai perché un server sequenziale non basta.

## Esempio

Ingresso:

```text
3
5 2 4
```

Uscita:

```text
cliente 1 attesa 0
cliente 2 attesa 5
cliente 3 attesa 7
attesa totale 12
```

## Come si lavora

1. `fauser nuovo C11 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

# C50 · Intestazioni di una mail

- **Materia:** TPSIT, anno scolastico 2027-28 · **L50** (slot 50 del programma `programmazione/TPSIT5.md`, data ipotetica 2028-04-06) · slide: `materiali/tpsit5/p32/L50-broker-e-code-di-messaggi/`
- **Compito della lezione 50**, per preparare la lezione 51 · Posta elettronica: SMTP e POP3.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C50-2028-04-06-intestazioni-mail/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un messaggio di posta è fatto da **intestazioni** (`Nome: valore`, una per riga), una **riga vuota** e il **corpo**. Leggi un messaggio e stampa mittente, destinatario, oggetto e quante righe ha il corpo.

## Ingresso

Intestazioni `From:`, `To:`, `Subject:` (in qualunque ordine), riga vuota, corpo. Gli indirizzi sono finti (dominio `example.invalid`).

## Uscita

Una riga: `da X a Y oggetto Z righe N`.

## Vincoli

Prepara la lezione 51: SMTP e POP3 parlano proprio con questo formato.

## Esempio

Ingresso:

```text
From: a@example.invalid
To: b@example.invalid
Subject: prova

ciao
buona giornata
```

Uscita:

```text
da a@example.invalid a b@example.invalid oggetto prova righe 2
```

## Come si lavora

1. `fauser nuovo C50 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

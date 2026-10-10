# C06 · Servizi e porte

- **Materia:** TPSIT, anno scolastico 2027-28 · **L06** (slot 6 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-09-30) · slide: `materiali/tpsit5/p32/L06-executor-lock-semafori/`
- **Compito della lezione 06**, per preparare la lezione 09 · Client-server e socket.
- **Cartella della consegna:** `tpsit/2027-28/compiti/C06-2027-09-30-servizi-e-porte/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Data una porta, di' quale servizio la usa di solito, con questa tabella: 22 SSH, 25 SMTP, 53 DNS, 80 HTTP, 443 HTTPS, 3306 MariaDB, 8080 Tomcat. Una porta che non è in tabella è `sconosciuta`.

## Ingresso

Numeri di porta separati da spazi o a capo.

## Uscita

Per ogni porta `porta servizio`.

## Vincoli

Prepara la lezione 9: leggi le pagine 164-170 del vol. 3.

## Esempio

Ingresso:

```text
80 443 22
```

Uscita:

```text
80 HTTP
443 HTTPS
22 SSH
```

## Come si lavora

1. `fauser nuovo C06 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

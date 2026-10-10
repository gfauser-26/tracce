# E25 · Chat: i messaggi a tutti

- **Materia:** TPSIT, anno scolastico 2027-28 · **L15** (slot 15 del programma `programmazione/TPSIT5.md`, data ipotetica 2027-11-01) · slide: `materiali/tpsit5/p32/L15-chat-tcp/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E25-2027-11-01-chat-broadcast/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Un server di chat TCP (socket veri su `127.0.0.1`, porta 0) tiene l'elenco dei client collegati. Ogni client si presenta con il suo nome. Quando uno scrive, il server manda il messaggio a **tutti gli altri**. Nel programma i client sono simulati: la prima riga di ingresso elenca i nomi; le righe successive sono `mittente testo`.

## Ingresso

Prima riga: i nomi dei client, separati da spazio. Poi righe `mittente testo` (il testo può contenere spazi).

## Uscita

Per ogni messaggio e per ogni altro client, **nell'ordine dei nomi**: `destinatario riceve mittente: testo`.

## Vincoli

Ogni client ha il suo socket e legge dal suo flusso. Il server tiene una mappa nome → flusso di uscita, protetta (`ConcurrentHashMap` o lucchetto).

## Esempio

Ingresso:

```text
anna bruno carla
anna ciao a tutti
bruno eccomi
```

Uscita:

```text
bruno riceve anna: ciao a tutti
carla riceve anna: ciao a tutti
anna riceve bruno: eccomi
carla riceve bruno: eccomi
```

## Come si lavora

1. `fauser nuovo E25 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

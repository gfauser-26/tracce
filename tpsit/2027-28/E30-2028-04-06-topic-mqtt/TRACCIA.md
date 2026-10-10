# E30 · Argomenti MQTT: chi riceve cosa

- **Materia:** TPSIT, anno scolastico 2027-28 · **L50** (slot 50 del programma `programmazione/TPSIT5.md`, data ipotetica 2028-04-06) · slide: `materiali/tpsit5/p32/L50-broker-e-code-di-messaggi/`
- **Cartella della consegna:** `tpsit/2027-28/esercizi/E30-2028-04-06-topic-mqtt/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Simula un piccolo **broker MQTT** in memoria. I client si iscrivono con dei **filtri** (`+` = un livello, `#` = tutto il resto, solo in coda). Quando arriva un messaggio, lo riceve ogni client con **almeno un filtro** che corrisponde al topic (una sola volta per client). `PUBR` pubblica e fa **conservare** l'ultimo messaggio di quel topic (*retained*): un nuovo iscritto lo riceve subito.

## Ingresso

Un comando per riga: `SUB client filtro`, `UNSUB client filtro`, `PUB topic testo`, `PUBR topic testo`. Il testo può avere spazi.

## Uscita

`SUB` e `UNSUB` → `OK` (`UNSUB` di un'iscrizione che non c'è → `ERR sconosciuto`). Per ogni messaggio ricevuto: `client riceve topic: testo`, nell'ordine di prima iscrizione che corrisponde; se nessuno lo riceve `nessuno`. Dopo un `SUB` si stampano prima `OK` e poi i messaggi *retained* che corrispondono, nell'ordine in cui sono stati conservati per la prima volta. Comando che non esiste → `ERR comando sconosciuto`.

## Vincoli

Riusa la funzione `corrisponde(filtro, topic)` dell'esempio della lezione (esempi-codice/mqtt-filtro). Nessun socket.

## Esempio

Ingresso:

```text
SUB a casa/+/luce
PUB casa/cucina/luce on
PUB casa/cucina/gas off
```

Uscita:

```text
OK
a riceve casa/cucina/luce: on
nessuno
```

## Come si lavora

1. `fauser nuovo E30 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento, input vuoto).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

# E13 · Lettori e scrittori con statistiche

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA5 Comunicazione e sincronizzazione**
- **Lezione:** 4BIN n. 44 (gio 01/04) · slide: `materiali/tpsit4/p32/lettori-scrittori/`
- **Cartella della consegna:** `tpsit/2026-27/esercizi/E13-2027-04-01-lettori-scrittori-letture/`
- **Linguaggio:** quello che hai scelto (uno degli 8 ammessi: C, C++, C#, Java, Python, Go, TypeScript, JavaScript), scritto in `lang.txt`.

## Consegna

Come nell'esempio della lezione: `w` scrittori (ognuno `m` volte: incrementa `a`, aspetta 1 ms, incrementa `b`) e `r` lettori (ognuno **30** letture: legge `a` e `b` e controlla che siano uguali). Usa lo schema con i semafori (il primo lettore chiude la porta agli scrittori, l'ultimo la riapre). In più conta il **numero totale di letture** fatte da tutti i lettori.

## Ingresso

Una riga: `w m r`.

## Uscita

Tre righe: `valore finale: V`, `letture: L`, `incoerenze: I` (V = w * m, L = r * 30, I = 0).

## Vincoli

1 <= w, r <= 8; 1 <= m <= 20. Il contatore delle letture va protetto.

## Esempio

Ingresso:

```text
2 3 3
```

Uscita:

```text
valore finale: 6
letture: 90
incoerenze: 0
```

## Come si lavora

1. `fauser nuovo E13 --materia tpsit` crea la cartella e scarica questa traccia e i test pubblici.
2. Scrivi il codice in `src/` (il file principale ha il nome fisso del tuo linguaggio, vedi `FLUSSO.md`).
3. `fauser test` esegue i test pubblici in `tests/` e scrive `.esito`.
4. `fauser consegna` quando passano.

Il programma legge dallo **standard input** e scrive sullo **standard output**; niente messaggi come «Inserisci...». L'uscita deve essere **identica** a quella attesa (righe, spazi, a capo finale).

## Test

- `tests/`: i casi **pubblici** (`01.in`/`01.out`, `02.in`/`02.out`): li vedi e li esegui con `fauser test`.
- `tests-nascosti/`: altri casi, solo del docente: li usa `make verifica-consegne` nella correzione. Passare i pubblici non basta: pensa ai casi limite (numeri negativi, valori estremi, un solo elemento).

## Uso dell'AI

Nel `README.md` della tua consegna scrivi se e come hai usato l'AI. Devi saper spiegare il tuo codice riga per riga.

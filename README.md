# tracce

Le **tracce** e i **test pubblici** di esercizi, compiti e verifiche delle classi del prof. Garofalo (a.s. 2026-27).

> **Non serve clonarlo né scaricare file a mano.** Ci pensa [`fauser`](https://github.com/gfauser-26/fauser):
>
> ```bash
> fauser nuovo <ID> --materia <materia>
> ```
>
> crea la cartella nel tuo repository `fauser-<username>` e ci copia traccia, test e allegati.

Qui puoi **leggere** una traccia in anticipo, per esempio dal telefono o prima di una verifica.

---

## Come è organizzato

```text
tracce/
├── indice.json                         l'elenco di tutte le tracce (lo legge fauser)
├── tpsit/
│   └── 2026-27/
│       └── C01-2027-05-25-dataviz-libreria-a-scelta/
│           ├── TRACCIA.md              la consegna: leggila tutta
│           ├── tests/                  i casi pubblici 01.in / 01.out ...
│           ├── controlli.json          (solo consegne web) i controlli di struttura
│           └── allegati/               file di partenza, per esempio dati.json
├── informatica/
│   └── 2026-27/ ...
└── gpoi/
    └── 2026-27/ ...
```

Il nome della cartella è sempre `<ID>-<AAAA-MM-GG>-<titolo>`:

| ID | Che cos'è | Dove finisce nel tuo repository |
|---|---|---|
| `E01`, `E02`... | esercizio | `<materia>/2026-27/esercizi/` |
| `C01`, `C02`... | compito per casa | `<materia>/2026-27/compiti/` |
| `V1`, `V2`... | verifica (una cartella `es1/`, `es2/`... per esercizio) | `<materia>/2026-27/verifiche/` |

La data è quella della lezione o della consegna. La **scadenza** precisa (giorno e ora) è scritta nella traccia.

---

## Come leggere una traccia

Ogni `TRACCIA.md` ha più o meno queste parti:

- **Materia, UdA e lezione** a cui si collega.
- **Linguaggio**: libero tra gli otto ammessi, se non è indicato diversamente.
- **Consegna**: cosa deve fare il programma.
- **Input e output**: il formato esatto. Il programma legge da standard input e scrive su standard output, **senza messaggi in più**.
- **Cosa consegnare**: i file e il README.
- **Scadenza** e, nelle verifiche, le **regole** (di solito niente chat, niente AI, niente condivisione del codice).

### I test pubblici

`tests/01.in` è l'input, `tests/01.out` l'output atteso. Prova il tuo programma con `fauser test`. Sono **solo una parte** dei casi: il docente ricontrolla ogni consegna anche con **test nascosti**, che non sono in questo repository. Pensa da solo ai casi limite: zero, negativi, input vuoto, valori grandi, ripetizioni.

### Gli allegati

I file in `allegati/` (per esempio `dati.json`) arrivano nella tua cartella **senza** il prefisso `allegati/`: `allegati/dati.json` diventa `<consegna>/dati.json`. `fauser` non sovrascrive mai un tuo file già esistente.

---

## Regole

- Questo repository è **in sola lettura** per gli studenti: niente issue o pull request con le soluzioni. Per dubbi su una traccia, chiedi al docente o su Discord.
- Le tracce possono essere corrette dopo la pubblicazione (un refuso, un caso sbagliato). Se il docente lo annuncia, rilancia `fauser nuovo`: i file che hai già scritto non vengono toccati.
- Non pubblicare le tue soluzioni in repository pubblici: il tuo lavoro va solo nel tuo `fauser-<username>`, che è privato.

---

## Vedi anche

- [La pagina dell'organizzazione](https://github.com/gfauser-26): il flusso completo e le regole.
- [`fauser`](https://github.com/gfauser-26/fauser): installazione e comandi.
- Leggere il Markdown: [guida rapida di GitHub](https://docs.github.com/it/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) (serve anche per scrivere il tuo `README.md`).

---

<sub>Per il docente: il repository si aggiorna con `make tracce-prepara DA=<sorgente> A=<clone di tracce>`, che copia solo i file pubblici e rigenera `indice.json`. Non va mai aggiornato a mano, e qui non devono mai finire `tests-nascosti/` o soluzioni.</sub>

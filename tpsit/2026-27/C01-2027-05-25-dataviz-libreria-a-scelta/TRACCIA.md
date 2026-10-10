# C01 · Data visualization: scegli la tua libreria

- **Materia:** TPSIT, anno scolastico 2026-27 · **UdA6 Frontend data-driven e React**
- **Lezione:** 4BIN n. 59 (mar 25/05), 4DIN n. 28 (lun 17/05, sfida facoltativa) · slide: `materiali/tpsit4/p32/chartjs/`
- **Cartella della consegna:** `tpsit/2026-27/compiti/C01-2027-05-25-dataviz-libreria-a-scelta/`
- **Linguaggio:** JavaScript nel browser (in `lang.txt` scrivi `web`).

## Consegna

Hai fatto un grafico con Chart.js. Ora scegli **una libreria di data visualization diversa**, più potente o più divertente, e rifai il grafico con lo stesso dataset (`dati.json`, fornito con la traccia). Poi vai oltre: un secondo tipo di grafico, interazione, animazione o un'idea tua.

### La rosa (scegline una)

| Libreria | Perché è interessante |
|---|---|
| **D3.js** | Il "linguaggio di montaggio" della visualizzazione: disegni tu ogni barra e ogni asse, controllo totale (curva di apprendimento ripida). |
| **Apache ECharts** | Tantissimi tipi di grafico pronti (mappe, radar, sankey), animazioni e tooltip belli senza fatica. |
| **Observable Plot** | Grafici eleganti con poche righe, pensato per esplorare dati: dal dato al grafico in 5 righe. |
| **Vega-Lite** | Descrivi il grafico con un JSON dichiarativo (dati, segni, assi) e la libreria fa il resto: interazioni incluse. |
| **Plotly.js** | Grafici interattivi pronti (zoom, hover, 3D, statistici), usati anche nella ricerca. |
| **p5.js** | Visualizzazione **creativa**: disegni sul canvas come in un gioco, il dato diventa forma, colore, movimento. |

Se vuoi un'altra libreria, chiedila al docente prima.

## Dataset

`dati.json` (nella cartella della consegna), lo stesso del compito con Chart.js: elenco di oggetti `{ "mese": ..., "vendite": ... }`. I dati sono inventati. Il file va **caricato con `fetch`**, non copiato dentro il codice. Puoi aggiungere campi o altri file di dati solo in aggiunta.

## Cosa consegnare

```
C01-2027-05-25-dataviz-libreria-a-scelta/
├── lang.txt        web
├── dati.json       il dataset (non modificare i dati esistenti)
├── index.html      la pagina con il grafico
├── src/            script e stili (facoltativo, se non li metti in index.html)
└── README.md       vedi sotto
```

La libreria si può caricare da CDN o scaricare: scrivi nel README quale e da dove. Per vedere la pagina serve un server locale (`python3 -m http.server`), perché `fetch` non legge i file aperti con doppio clic.

### README.md (obbligatorio, scritto da te)

1. **Quale libreria hai scelto e perché** (3-5 righe, con parole tue).
2. **Cosa hai scoperto**: una cosa che Chart.js non fa, o fa peggio, o una difficoltà che hai incontrato e come l'hai risolta.
3. **Cosa hai aggiunto** oltre al grafico base.
4. **Uso dell'AI**: se e come l'hai usata. Devi saper spiegare il codice riga per riga.
5. Fonti: documentazione o esempi da cui sei partito (non copiare un esempio intero senza dirlo).

## Come si controlla

L'uscita è grafica: **non ci sono test `.in`/`.out`** e `tests/` non è richiesta. `fauser test` fa solo un **controllo di struttura**: esistono `README.md` (non vuoto), `index.html` e `dati.json`, e `index.html` o i file in `src/` contengono una chiamata a `fetch` che nomina `dati.json`. Passarlo non vuol dire che il grafico sia bello o giusto: la valutazione è del docente, a vista, con la checklist qui sotto (nota per il docente).

<!--
Nota per il docente: checklist di valutazione (griglia a 4 livelli per voce, 0-3)

1. Funziona: aprendo la pagina da un server locale il grafico compare, senza errori in console. (peso alto)
2. Dati: carica dati.json con fetch, nessun valore copiato nel codice; i dati sono letti, non inventati.
3. Corretto: etichette, assi e valori corrispondono al dataset (controlla due punti a campione); titolo e leggenda leggibili.
4. Libreria usata davvero: non è Chart.js; l'uso è coerente con la libreria (non un wrapper di Chart.js).
5. Oltre il base: almeno un elemento in più (secondo tipo di grafico, tooltip/zoom/animazione, o idea creativa).
6. README: scelta motivata, scoperta concreta (non generica), uso dell'AI dichiarato.
7. Comprensione: lo studente sa spiegare 3 righe a scelta del proprio codice (domanda a voce, 2 minuti).
8. Ordine: struttura della cartella rispettata, commit con messaggio "C01: ...".

Segnali di allarme: README generico o identico a un altro; codice che lo studente non sa spiegare; libreria caricata ma grafico fatto con Chart.js; dati copiati nel codice.
Se due consegne sono troppo simili se ne parla a voce (regola del flusso).
Per 4DIN è facoltativo: si valuta come bonus, senza penalita'.
Il controllo di struttura lo fa `fauser test` con le regole di `controlli.json` (scaricato da `fauser nuovo`); alla correzione lo riesegue `verifica-consegne` con le regole originali.
-->

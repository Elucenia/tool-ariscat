<!-- ELUCENIA technical documentation · ariscat · it · no clinical/professional/rights approval -->

# ARISCAT

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/ariscat)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Età

`idade`

- `0` — ≤ 50 anni
- `3` — 51 a 80 anni
- `16` — \> 80 anni

### Saturazione di ossigeno preoperatoria (aria ambiente, a riposo)

`sat`

- `0` — ≥ 96%
- `8` — 91 a 95%
- `24` — ≤ 90%

### Infezione respiratoria nell’ultimo mese

`infec`

### Anemia preoperatoria (Hb ≤ 10 g/dL)

`anemia`

### Sede dell’incisione

`incisao`

- `0` — Periferica
- `15` — Addominale superiore
- `24` — Intratoracica

### Durata dell’intervento

`duracao`

- `0` — ≤ 2 h
- `16` — \> 2 h e ≤ 3 h
- `23` — \> 3 h

### Chirurgia d’emergenza

`emerg`

## Edizione del metodo

ARISCAT/Canet 2010, Tabella 6: 7 fattori ponderati; durata ≤ 2 h = 0, \> 2 h e ≤ 3 h = 16, \> 3 h = 23

## Formula documentata

Età 51–80 = 3, \> 80 = 16 · SpO₂ 91–95% = 8, ≤ 90% = 24 · infezione respiratoria nell’ultimo mese = 17 · Hb ≤ 10 g/dL = 11 · incisione addominale superiore = 15, intratoracica = 24 · durata ≤ 2 h = 0, \> 2 h e ≤ 3 h = 16, \> 3 h = 23 · chirurgia d’urgenza = 8.

## Limiti e popolazione

L’ARISCAT 2010 è stato derivato e validato in una coorte di 2464 pazienti chirurgici di 59 ospedali, con anestesia generale, neurassiale o regionale e complicanze polmonari postoperatorie come esito. L’età minima, le esclusioni e i pesi/intervalli completi non sono disponibili nell’abstract letto; i tassi della coorte non costituiscono una stima individuale ricalibrata per un’altra popolazione. Nella nuova lettura dell’articolo originale del 2010, i Metodi descrivono adulti di almeno 18 anni ed esclusioni proprie della coorte; la Tabella 6 conferma durata ≤2 h, \>2 fino a ≤3 h e \>3 h. La soglia di rischio alto è ≥45 nella Tabella 7 e \>45 nel testo; questa discrepanza documentale non è stata risolta qui.

## Riferimenti

- [Canet J et al. Prediction of postoperative pulmonary complications in a population-based surgical cohort. Anesthesiology, 2010.](https://doi.org/10.1097/ALN.0b013e3181fc6e0a)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

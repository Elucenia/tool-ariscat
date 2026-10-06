<!-- ELUCENIA technical documentation · ariscat · en · no clinical/professional/rights approval -->

# ARISCAT

[conditions, sources and permissions](https://elucenia.org/en/tools/ariscat)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Age

`idade`

- `0` — ≤ 50 years
- `3` — 51 to 80 years
- `16` — \> 80 years

### Preoperative oxygen saturation (room air, at rest)

`sat`

- `0` — ≥ 96%
- `8` — 91 to 95%
- `24` — ≤ 90%

### Respiratory infection in the last month

`infec`

### Preoperative anemia (Hb ≤ 10 g/dL)

`anemia`

### Incision site

`incisao`

- `0` — Peripheral
- `15` — Upper abdominal
- `24` — Intrathoracic

### Duration of surgery

`duracao`

- `0` — ≤ 2 h
- `16` — \> 2 h and ≤ 3 h
- `23` — \> 3 h

### Emergency surgery

`emerg`

## Method edition

ARISCAT/Canet 2010, Table 6: 7 weighted factors; duration ≤ 2 h = 0, \> 2 h and ≤ 3 h = 16, \> 3 h = 23

## Documented formula

Age 51–80 = 3, \> 80 = 16 · SpO₂ 91–95% = 8, ≤ 90% = 24 · respiratory infection in the past month = 17 · Hb ≤ 10 g/dL = 11 · upper abdominal incision = 15, intrathoracic incision = 24 · duration ≤ 2 h = 0, \> 2 h and ≤ 3 h = 16, \> 3 h = 23 · emergency surgery = 8.

## Limits and population

ARISCAT 2010 was derived and validated in a cohort of 2464 surgical patients at 59 hospitals, under general, neuraxial or regional anesthesia, with postoperative pulmonary complications as the outcome. The minimum age, exclusions and complete weights/ranges are not available in the abstract read; the cohort rates are not an individual estimate recalibrated for another population. The new reading of the original 2010 article found that the Methods describe adults aged at least 18 and study-specific exclusions; Table 6 confirms duration ≤2 h, \>2 to ≤3 h and \>3 h. The high-risk boundary is ≥45 in Table 7 and \>45 in the text; this documentary discrepancy has not been adjudicated here.

## References

- [Canet J et al. Prediction of postoperative pulmonary complications in a population-based surgical cohort. Anesthesiology, 2010.](https://doi.org/10.1097/ALN.0b013e3181fc6e0a)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Documented results

The information below preserves the method outputs for synthetic examples. It does not constitute independent clinical validation.

### 1

Low risk (< 26): 1.6% pulmonary complications

Usual care.


### 2

Intermediate risk (26 to 44): 13.3% pulmonary complications

Consider lung-protective strategies and respiratory physiotherapy.


### 3

Intermediate risk (26 to 44): 13.3% pulmonary complications

Consider lung-protective strategies and respiratory physiotherapy.


### 4

High risk (≥ 45): 42.1% pulmonary complications

Optimize before surgery, protective ventilation, cough-sparing analgesia and early mobilization.


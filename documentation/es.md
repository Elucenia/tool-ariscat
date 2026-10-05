<!-- ELUCENIA technical documentation · ariscat · es · no clinical/professional/rights approval -->

# ARISCAT

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/ariscat)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Edad

`idade`

- `0` — ≤ 50 años
- `3` — 51 a 80 años
- `16` — \> 80 años

### Saturación de oxígeno preoperatoria (aire ambiente, en reposo)

`sat`

- `0` — ≥ 96%
- `8` — 91 a 95%
- `24` — ≤ 90%

### Infección respiratoria en el último mes

`infec`

### Anemia preoperatoria (Hb ≤ 10 g/dL)

`anemia`

### Localización de la incisión

`incisao`

- `0` — Periférica
- `15` — Abdominal alta
- `24` — Intratorácica

### Duración de la cirugía

`duracao`

- `0` — ≤ 2 h
- `16` — \> 2 h y ≤ 3 h
- `23` — \> 3 h

### Cirugía de emergencia

`emerg`

## Edición del método

ARISCAT/Canet 2010, Tabla 6: 7 factores ponderados; duración ≤ 2 h = 0, \> 2 h y ≤ 3 h = 16, \> 3 h = 23

## Fórmula documentada

Edad 51–80 = 3, \> 80 = 16 · SpO₂ 91–95% = 8, ≤ 90% = 24 · infección respiratoria en el último mes = 17 · Hb ≤ 10 g/dL = 11 · incisión abdominal superior = 15, intratorácica = 24 · duración ≤ 2 h = 0, \> 2 h y ≤ 3 h = 16, \> 3 h = 23 · cirugía de urgencia = 8.

## Límites y población

El ARISCAT 2010 se derivó y validó en una cohorte de 2464 pacientes quirúrgicos de 59 hospitales, con anestesia general, neuroaxial o regional, y complicaciones pulmonares posoperatorias como desenlace. La edad mínima, las exclusiones y los pesos/intervalos completos no están disponibles en el resumen leído; las tasas de la cohorte no constituyen una estimación individual recalibrada para otra población. En la nueva lectura del artículo original de 2010, los Métodos describen adultos de al menos 18 años y exclusiones propias de la cohorte; la Tabla 6 confirma duración ≤2 h, \>2 a ≤3 h y \>3 h. El límite de riesgo alto figura como ≥45 en la Tabla 7 y \>45 en el texto; esta discrepancia documental no se ha resuelto aquí.

## Referencias

- [Canet J et al. Prediction of postoperative pulmonary complications in a population-based surgical cohort. Anesthesiology, 2010.](https://doi.org/10.1097/ALN.0b013e3181fc6e0a)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

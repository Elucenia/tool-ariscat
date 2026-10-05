<!-- ELUCENIA technical documentation · ariscat · pt-BR · no clinical/professional/rights approval -->

# ARISCAT

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/ariscat)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Idade

`idade`

- `0` — ≤ 50 anos
- `3` — 51 a 80 anos
- `16` — \> 80 anos

### SatO₂ pré-operatória (ar ambiente, em repouso)

`sat`

- `0` — ≥ 96%
- `8` — 91 a 95%
- `24` — ≤ 90%

### Infecção respiratória no último mês

`infec`

### Anemia pré-operatória (Hb ≤ 10 g/dL)

`anemia`

### Local da incisão

`incisao`

- `0` — Periférica
- `15` — Abdominal alta
- `24` — Intratorácica

### Duração da cirurgia

`duracao`

- `0` — ≤ 2 h
- `16` — \> 2 h e ≤ 3 h
- `23` — \> 3 h

### Cirurgia de emergência

`emerg`

## Edição do método

ARISCAT/Canet 2010, Tabela 6: 7 fatores ponderados; duração ≤ 2 h = 0, \> 2 h e ≤ 3 h = 16, \> 3 h = 23

## Fórmula documentada

Idade 51–80 = 3, \> 80 = 16 · SatO₂ 91–95% = 8, ≤ 90% = 24 · infecção respiratória no último mês = 17 · Hb ≤ 10 g/dL = 11 · incisão abdominal alta = 15, intratorácica = 24 · duração ≤ 2 h = 0, \> 2 h e ≤ 3 h = 16, \> 3 h = 23 · emergência = 8.

## Limites e população

O ARISCAT 2010 foi derivado e validado em uma coorte de 2464 pacientes cirúrgicos de 59 hospitais, com anestesia geral, neuraxial ou regional, e desfecho de complicações pulmonares pós-operatórias. A idade mínima, exclusões e pesos/faixas completos não estão disponíveis no resumo lido; as taxas da coorte não constituem uma estimativa individual recalibrada para outra população. Na nova leitura do artigo original de 2010, os Métodos descrevem adultos com pelo menos 18 anos e exclusões próprias da coorte; a Tabela 6 confirma duração ≤2 h, \>2 a ≤3 h e \>3 h. A fronteira de alto risco aparece como ≥45 na Tabela 7 e \>45 no texto; essa divergência documental não foi adjudicada aqui.

## Referências

- [Canet J et al. Prediction of postoperative pulmonary complications in a population-based surgical cohort. Anesthesiology, 2010.](https://doi.org/10.1097/ALN.0b013e3181fc6e0a)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

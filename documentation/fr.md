<!-- ELUCENIA technical documentation · ariscat · fr · no clinical/professional/rights approval -->

# ARISCAT

[conditions, sources et autorisations](https://elucenia.org/fr/outils/ariscat)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Âge

`idade`

- `0` — ≤ 50 ans
- `3` — 51 à 80 ans
- `16` — \> 80 ans

### Saturation préopératoire en oxygène (air ambiant, au repos)

`sat`

- `0` — ≥ 96%
- `8` — 91 à 95%
- `24` — ≤ 90%

### Infection respiratoire au cours du dernier mois

`infec`

### Anémie préopératoire (Hb ≤ 10 g/dL)

`anemia`

### Site de l’incision

`incisao`

- `0` — Périphérique
- `15` — Abdominale haute
- `24` — Intrathoracique

### Durée de l’intervention

`duracao`

- `0` — ≤ 2 h
- `16` — \> 2 h et ≤ 3 h
- `23` — \> 3 h

### Chirurgie en urgence

`emerg`

## Édition de la méthode

ARISCAT/Canet 2010, Tableau 6 : 7 facteurs pondérés ; durée ≤ 2 h = 0, \> 2 h et ≤ 3 h = 16, \> 3 h = 23

## Formule documentée

Âge 51–80 = 3, \> 80 = 16 · SpO₂ 91–95% = 8, ≤ 90% = 24 · infection respiratoire au cours du dernier mois = 17 · Hb ≤ 10 g/dL = 11 · incision abdominale haute = 15, intrathoracique = 24 · durée ≤ 2 h = 0, \> 2 h et ≤ 3 h = 16, \> 3 h = 23 · chirurgie en urgence = 8.

## Limites et population

L’ARISCAT 2010 a été développé et validé dans une cohorte de 2464 patients chirurgicaux de 59 hôpitaux, sous anesthésie générale, neuraxiale ou régionale, avec comme critère de jugement les complications pulmonaires postopératoires. L’âge minimal, les exclusions et les pondérations et intervalles complets ne figurent pas dans le résumé lu ; les taux de la cohorte ne constituent pas une estimation individuelle recalibrée pour une autre population. La nouvelle lecture de l’article original de 2010 montre que les Méthodes décrivent des adultes d’au moins 18 ans et des exclusions propres à la cohorte ; le Tableau 6 confirme les durées ≤2 h, \>2 à ≤3 h et \>3 h. Le seuil de risque élevé est ≥45 dans le Tableau 7 et \>45 dans le texte ; cette divergence documentaire n’a pas été tranchée ici.

## Références

- [Canet J et al. Prediction of postoperative pulmonary complications in a population-based surgical cohort. Anesthesiology, 2010.](https://doi.org/10.1097/ALN.0b013e3181fc6e0a)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Résultats documentés

Les informations ci-dessous conservent les sorties de la méthode pour des exemples synthétiques. Elles ne constituent pas une validation clinique indépendante.

### 1

Faible risque (< 26) : 1,6 % de complications pulmonaires

Soins habituels.


### 2

Risque intermédiaire (26 à 44) : 13,3 % de complications pulmonaires

Envisager des stratégies de protection pulmonaire et une kinésithérapie respiratoire.


### 3

Risque intermédiaire (26 à 44) : 13,3 % de complications pulmonaires

Envisager des stratégies de protection pulmonaire et une kinésithérapie respiratoire.


### 4

Risque élevé (≥ 45) : 42,1 % de complications pulmonaires

Optimiser avant la chirurgie, ventilation protectrice, analgésie épargnant la toux et mobilisation précoce.


### 7. Évaluer une IA au-delà de sa performance globale

Le modèle a correctement prédit que 90 patients ne seraient pas réhospitalisés. Il n’a toutefois repéré **aucun des 10 patients réhospitalisés**. Ces 10 patients manqués sont des **faux négatifs**.

Le **rappel**, aussi appelé **sensibilité**, est plus utile ici. Il mesure la part des patients réellement réhospitalisés que le modèle a repérés.

**Rappel = patients repérés parmi les réhospitalisés ÷ nombre total de patients réhospitalisés.**

Dans cet exemple, le rappel est de **0 sur 10, soit 0 %**, malgré 90 % de prédictions correctes.

#### Comparer les tranches d’âge

Sur un jeu de test, applique le même seuil de décision à toutes les tranches d’âge. Pour chaque tranche, divise le nombre de patients manqués par le nombre de patients réellement réhospitalisés.

| Tranche d’âge | Patients réhospitalisés | Patients manqués | Part manquée |
|---|---:|---:|---:|
| Moins de 65 ans | 20 | 4 | 20 % |
| 65 ans et plus | 10 | 5 | 50 % |

Dans cet exemple fictif, le modèle manque une plus grande **proportion** de patients chez les 65 ans et plus. Il faut aussi regarder les effectifs, car quelques cas peuvent faire beaucoup varier le pourcentage dans un petit groupe.


#### Source

- [Google for Developers — Exactitude, précision et rappel](https://developers.google.com/machine-learning/crash-course/classification/accuracy-precision-recall)
# 8. Appliquer les notions à un projet

## Recommandation à l'hôpital

L'hôpital peut **préparer puis tester** l'IA dans un cadre limité, mais ne devrait pas s'en servir immédiatement pour décider seuls quels patients rappeler. Un appel de suivi est une décision humaine qui touche à la santé : toute prédiction doit être vérifiée et mise sous supervision médicale.

Le test conseillé est un **pilote contrôlé** :

1. utiliser une population réelle ou représentative, uniquement à des fins définies ;
2. donner au médecin les résultats du modèle comme information d'aide, sans lui retirer la responsabilité ;
3. conserver une trace des prédictions, des décisions et des appels effectués ;
4. ne pas modifier le fonctionnement clinique à partir d'une seule mesure globale ;
5. arrêter ou suspendre le pilote si les erreurs ou les biais sont inacceptables.

## Données utilisables

Pour étudier le risque de réhospitalisation, l'équipe devrait commencer par les données nécessaires à cette finalité. Dans le cas présenté :

| Information | Utilisation possible |
|---|---|
| Identifiant pseudonymisé | Relier les séjours d'une même personne sans publier son nom |
| Date de sortie et date de réadmission | Calculer si la réadmission intervient dans les 30 jours |
| Indicateur « réhospitalisé dans les 30 jours » | Servir de variable cible après vérification de sa bonne définition |
| Tranche d'âge | Vérifier les performances et les éventuelles disparités |
| Variables cliniques précisément justifiées | Ajouter uniquement celles qui améliorent réellement la prédiction et dont l'utilisation est autorisée |

À défaut de justification, le nom, l'adresse, le numéro de téléphone, les diagnostics détaillés et les notes cliniques peuvent être écartés. Les variables restantes doivent être pseudonymisées, accessibles uniquement aux personnes autorisées et conservées aussi peu longtemps que possible.

Comme il s'agit de données de santé, le projet doit être fondé sur une base légale de l'article 6 du RGPD et sur une condition applicable au traitement des données de santé prévue à l'article 9. Une base juridique pour le soin ou la recherche, par exemple, ne peut être choisie automatiquement : elle dépend du statut de l'hôpital, de sa finalité réelle et du droit national applicable. Le responsable du traitement devrait aussi réaliser une analyse d'impact sur la protection des données si le traitement présente des risques élevés, consulter le DPD et documenter les mesures de sécurité.

## Vérification indispensable avant de se fier aux prédictions

L'indicateur pertinent n'est pas seulement l'exactitude globale. Avec 10 réhospitalisations sur 100 patients, un modèle qui ne signale personne peut être exact dans 90 cas tout en **ratant les 10 réhospitalisations**.

L'équipe doit donc mesurer au minimum :

- le **rappel (sensibilité)** : proportion des patients réellement réhospitalisés qui ont été identifiés ;
- la **précision** : proportion de patients rappelés qui sont réellement réhospitalisés ;
- les **faux négatifs** : réhospitalisations non détectées, particulièrement préjudiciables pour l'appel de suivi ;
- le **faux positifs** : appels inutiles et charge supplémentaire pour l'équipe ;
- la calibration : les probabilités annoncées correspondent-elles aux risques observés ?

Il faut vérifier ces mesures sur des données séparées de l'entraînement et, idéalement, par validation externe puis prospective. Il faut aussi comparer les résultats par tranches d'âge, sexe si légalement utilisé, commune ou autres sous-groupes pertinents, afin de détecter une sous-performance qui serait masquée par la moyenne globale.

Enfin, le seuil qui décide « rappeler » ou « ne pas rappeler » doit être fixé selon le coût comparé d'un appel manqué et d'un appel inutile. Modifier ce seuil n'améliore pas automatiquement le modèle : il déplace le compromis entre rappel et précision.

## Positionnement au titre de l'AI Act

Avant toute mise en œuvre, l'hôpital doit déterminer le rôle exact du système : aide à l'organisation des soins ou outil participant à une décision médicale. Selon sa fonction, sa certification éventuelle et son intégration dans un produit, le système pourrait relever d'obligations applicables aux systèmes à haut risque.

Il faudrait documenter au minimum :

- l'usage prévu et les utilisateurs concernés ;
- les groupes de patients susceptibles d'être affectés ;
- les limites connues du modèle ;
- la supervision humaine et les possibilités d'intervention ;
- la gestion des erreurs, des incidents et du maintien en fonctionnement ;
- la qualité des données d'entraînement et les règles de mise à jour ;
- la traçabilité, les journaux et la responsabilité de l'établissement.

Si le système est proposé par un fournisseur comme produit à usage médical, les obligations pourraient aussi concerner le fournisseur et l'établissement selon leur rôle réel.

## Informations encore nécessaires pour trancher

Il manque notamment :

- la finalité exacte : accompagnement du suivi, priorité d'appel, triage ou décision de soins ;
- la base légale RGPD retenue et la condition applicable aux données de santé ;
- la classification réglementaire du système au titre de l'AI Act ;
- le fournisseur, le modèle, son usage prévu et ses limites documentées ;
- la qualité et la représentativité des données d'entraînement ;
- les performances sur une population indépendante, séparées par tranches d'âge et autres groupes pertinents ;
- le seuil choisi, le coût des erreurs et le processus de supervision médicale ;
- le résultat de l'analyse d'impact, du point de vue RGPD et des règles applicables à l'IA.

## À retenir

- Commencer par une extraction minimale, pseudonymisée dès que possible.
- Utiliser l'IA comme aide à une décision humaine encadrée, pas comme décision autonome.
- Mesurer surtout les faux négatifs et le rappel, pas uniquement l'exactitude globale.
- Tester sur des données indépendantes et vérifier les performances dans chaque groupe de patients.
- Ne pas passer au déploiement avant d'avoir déterminé le cadre RGPD, les obligations AI Act et les risques résiduels.

## Question de vérification

Un modèle obtient une exactitude de 90 % sur 100 patients dont 10 sont réhospitalisés. Peut-on conclure qu'il identifie correctement les patients à rappeler ? Justifiez pourquoi.

<details>
<summary>Corrigé</summary>

Non. Une exactitude élevée peut masquer zéro rappel si le modèle prédit systématiquement « pas de réhospitalisation ». Il faut mesurer le rappel pour connaître le nombre de réhospitalisations réellement détectées, ainsi que la précision et les erreurs dans chaque sous-groupe. Un modèle utile doit aussi être validé sur des données indépendantes avant son utilisation clinique.

</details>

## Sources

- Règlement (UE) 2016/679 (RGPD), articles 5, 6, 9, 25 et 35 : https://www.cnil.fr/fr/reglement-europeen-protection-donnees/chapitre2
- CNIL, analyse d'impact relative à la protection des données : https://www.cnil.fr/fr/lanalyse-dimpact-sur-la-protection-des-donnees-a-caractere-personnel
- Règlement (UE) 2024/1689 (AI Act), exigences relatives aux systèmes à haut risque : https://eur-lex.europa.eu/eli/reg/2024/1689/oj
- Présentation de l'approche fondée sur les risques de l'AI Act : https://digital-strategy.ec.europa.eu/fr/policies/regulatory-framework-ai

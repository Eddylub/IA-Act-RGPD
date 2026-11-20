# 5. Protéger les personnes et organiser le travail

## Qui peut voir quelles données ?

Dans une équipe médicale, l'accès aux données ne doit pas dépendre uniquement du statut général d'une personne dans l'hôpital. Il doit être limité à **ce dont elle a besoin pour accomplir sa mission**. Cela relève du principe de minimisation et de la « protection des données par défaut » (RGPD, articles 25 et 32).

| Rôle dans l'équipe | Exemple d'accès adapté | Données à éviter |
|---|---|---|
| Médecin prenant en charge le patient | Consultation complète nécessaire à son diagnostic et à son suivi | Ne pas conserver plus longtemps que nécessaire les extractions utilisées hors du dossier |
| Infirmier ou infirmière assurant le suivi | Les informations utiles aux soins, prescriptions et observations relevant de sa mission | Historique ou données sans lien avec les soins confiés |
| Personnel administratif | Identité, coordonnées et données nécessaires à la prise de rendez-vous | Diagnostic, résultat détaillé ou autres données cliniques inutiles |
| Équipe de recherche ou service d'IA | Données minimisées, idéalement pseudonymisées | Accès au dossier complet ou à la table reliant les codes aux identités |
| Responsables techniques | Accès limité aux fonctions nécessaires à la maintenance | Droit de consulter les contenus patients sans raison de maintenance |

Les droits d'accès doivent être accordés individuellement, puis **révoqués lorsqu'ils ne sont plus nécessaires**. L'hôpital peut mettre en place :

- des rôles et profils d'accès ;
- une authentification forte, avec séparation des fonctions ;
- des journaux d'accès pour détecter les consultations abusives ;
- des mesures de chiffrement et de sauvegarde sécurisée ;
- la formation des professionnels au secret médical et à la manipulation des données ;
- des revues régulières des habilitations, notamment après un changement de poste ;
- pour les systèmes d'IA, des restrictions supplémentaires sur les jeux d'entraînement, les sorties et les traces produites.

En ce qui concerne l'AI Act, la protection suppose aussi que les personnes chargées de superviser un système d'IA puissent comprendre ses limites et intervenir. Lorsqu'un système d'IA relevant de règles de haut risque est utilisé en santé, les personnes compétentes chargées de la supervision doivent pouvoir surveiller son fonctionnement et décider de ne pas suivre une suggestion. L'outil ne remplace pas la responsabilité professionnelle du médecin.

## Que faire si un patient signale une erreur dans son dossier ?

Il peut exercer son **droit de rectification** : il a le droit d'obtenir, dans les meilleurs délais, que les données inexactes concernant sa personne soient corrigées (RGPD, article 16). Si certaines données sont incomplètes, il peut aussi demander leur complétude.

La demande peut être adressée à :

1. **le responsable du dossier ou l'établissement hospitalier**, par exemple le secrétariat du dossier patient, le service santé ou le guichet prévu par l'hôpital ;
2. **le délégué à la protection des données (DPD ou DPO) de l'hôpital**, si la demande concerne l'accès, la conservation, les traitements ou la rectification ;
3. **l'autorité de contrôle compétente**, en France la CNIL, si la demande n'obtient pas de réponse satisfaisante.

La rectification ne signifie pas forcément que toute donnée ancienne disparaît immédiatement : il peut être nécessaire de conserver une trace de la correction, par exemple pour assurer la traçabilité du dossier. Le responsable doit répondre en principe sous un mois ; ce délai peut être prolongé de deux mois dans certains cas complexes, avec information de la personne concernée.

Le patient peut également demander :

- l'accès à son dossier (article 15) ;
- l'effacement de certaines données, lorsque les conditions légales sont réunies (article 17) ;
- la limitation du traitement dans les situations prévues (article 18) ;
- une copie des données qu'il fournit sous une forme structurée et lisible (article 20), si les conditions s'appliquent.

## À retenir

- Chaque membre de l'équipe reçoit uniquement les accès nécessaires à sa mission.
- Les données médicales et les données utilisées par une IA doivent être protégées techniquement et organisées en rôles.
- Une IA peut assister un professionnel, mais elle ne doit pas supprimer sa capacité de contrôle humain.
- En cas d'information inexacte, le patient peut exercer son droit de rectification auprès de l'établissement ou du DPO.
- En cas de désaccord persistant, il peut saisir la CNIL.

## Question de vérification

Un stagiaire ou une secrétaire peut-il avoir accès au dossier médical complet d'un patient « pour se former » ou « pour comprendre le fonctionnement » ? Justifiez votre réponse.

<details>
<summary>Corrigé</summary>

Non, pas automatiquement. L'accès doit être proportionné à une mission réelle et autorisée. Les données utiles à la formation peuvent être remplacées par un dossier fictif ou une copie anonymisée/pseudonymisée. Si l'accès exceptionnel est nécessaire à une mission encadrée, il doit être limité, tracé et soumis aux autorisations appropriées.

</details>

## Sources

- RGPD, articles 16, 25 et 32 : https://www.cnil.fr/fr/reglement-europeen-protection-donnees/chapitre4
- CNIL, droits des personnes sur leurs données : https://www.cnil.fr/fr/les-droits-pour-les-personnes
- Règlement (UE) 2024/1689 (AI Act), notamment les exigences relatives à la supervision humaine pour les systèmes à haut risque : https://eur-lex.europa.eu/eli/reg/2024/1689/oj

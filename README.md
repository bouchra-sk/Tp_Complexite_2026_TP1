# TP N°1 – Test de primalité

<p align="center">
  <strong>Implémentation et analyse comparative de quatre algorithmes de test de primalité</strong>
</p>

---

## Présentation du TP

Ce TP porte sur l'étude de différentes approches algorithmiques permettant de déterminer si un entier naturel est un nombre premier.

L'objectif principal est d'implémenter quatre algorithmes en langage C, puis de comparer leurs performances à travers une analyse théorique et expérimentale de leur complexité temporelle.

Les mesures du temps d'exécution sont réalisées à l'aide des fonctions de la bibliothèque `time.h`, en faisant varier la taille des nombres testés.

## Objectifs

- Implémenter différentes méthodes de test de primalité.
- Comprendre l'impact des optimisations sur les performances d'un algorithme.
- Étudier les complexités temporelles théoriques.
- Mesurer les temps d'exécution pour différentes valeurs de N.
- Comparer les résultats théoriques et expérimentaux.
- Visualiser graphiquement l'évolution des performances des algorithmes.

## Les algorithmes étudiés

### A1 – Approche naïve

Le premier algorithme consiste à tester la divisibilité de N par tous les entiers compris entre 2 et N-1.

- Principe : tester chaque diviseur potentiel.
- Complexité temporelle au pire cas : O(N).

### A2 – Amélioration de l'approche naïve

Cette approche exploite la propriété selon laquelle tout diviseur propre d'un entier N est inférieur ou égal à N/2.

- Principe : limiter les tests de divisibilité jusqu'à N/2.
- Complexité temporelle au pire cas : O(N).

### A3 – Optimisation par la racine carrée

Cet algorithme exploite une propriété mathématique des diviseurs : si N possède un diviseur supérieur à √N, alors il possède nécessairement un diviseur inférieur à √N.

- Principe : tester uniquement les diviseurs jusqu'à √N.
- Complexité temporelle au pire cas : O(√N).

### A4 – Optimisation par élimination des nombres pairs

Cette approche améliore A3 en évitant les tests inutiles sur les nombres pairs.

- Vérifier d'abord si N est pair.
- Traiter directement le cas N = 2.
- Si N est impair, tester uniquement les diviseurs impairs jusqu'à √N.
- Complexité temporelle au pire cas : O(√N).

## Analyse expérimentale

Les quatre algorithmes sont testés sur un ensemble de nombres entiers de tailles croissantes.

Les expériences permettent d'étudier :

- La variation du temps d'exécution T(N).
- L'évolution des performances lorsque N augmente.
- L'influence des optimisations successives.
- La compatibilité entre les prédictions théoriques et les résultats expérimentaux.

### Comparaison des complexités théoriques

| Algorithme | Principe | Complexité au pire cas |
|---|---|---|
| A1 | Test jusqu'à N-1 | O(N) |
| A2 | Test jusqu'à N/2 | O(N) |
| A3 | Test jusqu'à √N | O(√N) |
| A4 | Test des diviseurs impairs jusqu'à √N | O(√N) |

## Technologies utilisées

| Technologie | Utilisation |
|---|---|
| C | Implémentation des algorithmes |
| GCC | Compilation et exécution |
| `time.h` | Mesure du temps d'exécution |
| Excel | Représentation graphique des résultats |
| Git & GitHub | Gestion et versionnement du projet |



## Conclusion

Ce TP permet de mettre en évidence l'importance de l'optimisation algorithmique dans la résolution d'un même problème.

Bien que les quatre algorithmes reposent sur le même principe de test de divisibilité, leurs performances diffèrent considérablement en fonction des optimisations appliquées.

L'analyse théorique, associée aux mesures expérimentales, permet de mieux comprendre l'évolution de la complexité et l'efficacité des différentes approches.
<p align="center">
  <i>TP réalisé dans le cadre du module Algorithmique Avancée et Complexité.</i>
</p>

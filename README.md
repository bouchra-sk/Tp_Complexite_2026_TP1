# TP – Algorithmique Avancée et Complexité

<p align="center">
  <strong>Étude et comparaison expérimentale des algorithmes de recherche et de recherche du minimum et du maximum</strong>
</p>

---

## Présentation du projet

Ce TP a pour objectif d'étudier la complexité algorithmique à travers l'implémentation et l'analyse de plusieurs algorithmes en langage C.

Il porte principalement sur deux problèmes : la recherche d'un élément dans un tableau et la recherche simultanée du minimum et du maximum d'un ensemble de valeurs.

Une attention particulière est accordée à la comparaison des performances théoriques et expérimentales des différentes approches.

## Objectifs

- Implémenter plusieurs méthodes de recherche dans des tableaux.
- Étudier les différences entre les meilleurs et les pires cas.
- Analyser les complexités temporelles des algorithmes.
- Comparer le nombre de comparaisons effectuées.
- Mesurer les temps d'exécution en fonction de la taille des données.
- Représenter graphiquement les résultats expérimentaux.

## Partie A – Recherche d'un élément

Cette partie étudie différentes méthodes permettant de rechercher une valeur donnée dans un tableau.

### 1. Recherche dans un tableau non trié

**Fonction :** `rechElets_TabNonTries`

Recherche séquentielle d'un élément dans un tableau non trié.

- Meilleur cas : O(1)
- Pire cas : O(n)

### 2. Recherche dans un tableau trié

**Fonction :** `rechElets_TabTries`

Recherche séquentielle optimisée exploitant l'ordre croissant des éléments pour arrêter la recherche dès que la valeur recherchée ne peut plus être présente.

- Meilleur cas : O(1)
- Pire cas : O(n)

### 3. Recherche dichotomique

**Fonction :** `rechElets_Dicho`

Cette méthode repose sur le principe de division de l'intervalle de recherche en deux parties à chaque étape.

Elle nécessite un tableau préalablement trié.

- Meilleur cas : O(1)
- Pire cas : O(log n)

### Analyse expérimentale

Les trois algorithmes sont évalués en faisant varier la taille des tableaux afin de mesurer leurs temps d'exécution dans les meilleurs et les pires cas.

Les résultats permettent d'étudier l'évolution du temps d'exécution et de comparer l'efficacité des différentes méthodes.

## Partie B – Recherche du minimum et du maximum

Cette partie consiste à déterminer simultanément les valeurs minimale et maximale d'un tableau non trié contenant des éléments distincts.

### 1. Approche naïve

**Fonction :** `MaxEtMinA`

L'approche naïve consiste à parcourir le tableau et à comparer chaque élément avec le minimum et le maximum actuellement connus.

- Complexité temporelle : O(n)
- Nombre de comparaisons : 2(n - 1)

### 2. Approche optimisée – Comparaison par paires

**Fonction :** `MaxEtMinB`

Cette approche améliore le nombre de comparaisons en procédant par paires :

1. Comparer les éléments deux à deux.
2. Identifier le plus petit et le plus grand de chaque paire.
3. Rechercher le minimum parmi les plus petits éléments.
4. Rechercher le maximum parmi les plus grands éléments.
5. Traiter séparément le dernier élément lorsque la taille du tableau est impaire.

- Complexité temporelle : O(n)
- Nombre de comparaisons au pire cas : environ 3n/2 - 2 (pour n pair).

### Comparaison des performances

Un compteur de comparaisons est intégré aux deux fonctions afin d'évaluer leur efficacité.

L'analyse expérimentale porte sur :

- Le nombre de comparaisons effectuées.
- Le temps d'exécution.
- L'évolution des performances selon la taille du tableau.

## Technologies utilisées

| Technologie | Utilisation |
|---|---|
| C | Implémentation des algorithmes |
| GCC | Compilation |
| Git & GitHub | Gestion et versionnement du code |
| Python / Matplotlib | Visualisation des résultats (si utilisés) |

## Analyse et résultats

Les expériences permettent de mettre en évidence les différences entre les approches étudiées, notamment en matière de nombre de comparaisons et de temps d'exécution.

Les tableaux et les représentations graphiques permettent de confronter les résultats expérimentaux aux complexités théoriques.




<p align="center">
  <i>TP réalisé dans le cadre du module Algorithmique Avancée et Complexité.</i>
</p>

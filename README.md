# TIPE_2026_2027
## THEME : Sobriété, Efficacité, Optimisation 
![Status](https://img.shields.io/badge/TIPE-2027-blue)
![Matière](https://img.shields.io/badge/Matière-Mathématiques%20%2F%20Physique-red)
![Outils](https://img.shields.io/badge/Outils-Python%20%2F%20Calcul%20Variationnel-green)

## Présentation du Projet
Ce projet de TIPE s'intéresse à la **Brachistochrone** (du grec *brakhistos* le plus court, et *chronos* le temps), la courbe entre deux points sur laquelle un mobile glissant sans frottement atteint le point bas le plus rapidement possible. 

Dans le cadre du thème **Sobriété, Efficacité, Optimisation**, ce travail ne se limite pas à la résolution historique de Bernoulli. Il explore comment l'**optimisation géométrique** permet d'atteindre une **efficacité de transfert énergétique** maximale, tout en étudiant l'impact des contraintes réelles (frottements) sur la **sobriété** du système.

## ❓ Problématique
> **Comment le calcul des variations permet-il de définir une trajectoire minimisant le temps de transfert, et dans quelle mesure l'introduction de frottements modifie-t-elle l'efficacité de cette solution optimale ?**

## 🛠️ Contenu du Dépôt
L'architecture de ce dépôt est organisée comme suit :

* `/Theorie` : Démonstration de l'équation d'Euler-Lagrange appliquée à la fonctionnelle du temps.
* `/Simulation` : Scripts Python permettant de modéliser la descente sur différentes courbes (droite, arc de cercle, cycloïde).
* `/Optimisation_Numerique` : Recherche de la courbe optimale par méthode de descente de gradient ou algorithmes génétiques en présence de frottements.
* `/Data` : Résultats des mesures expérimentales (acquisition vidéo).

## 🧮 Modélisation Mathématique
Le cœur du projet repose sur la minimisation de la fonctionnelle de temps $T[y]$ :

$$T[y] = \int_{x_A}^{x_B} \frac{\sqrt{1 + y'(x)^2}}{\sqrt{2gy(x)}} dx$$

L'application de l'équation d'**Euler-Lagrange** permet de montrer que la solution est une **cycloïde**. 
Mon étude compare cette solution idéale avec des modèles incluant :
1.  Le moment d'inertie d'une bille réelle ($E_c$ de rotation).
2.  Les frottements fluides et solides (perte d'efficacité).

## 🚀 Utilisation des scripts
Pour lancer la comparaison des trajectoires :
```bash
python Simulation/compare_curves.py

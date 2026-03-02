# TIPE_2026_2027
## THEME : Sobriété, Efficacité, Optimisation

## PROBLEMATIQUE
> **Comment optimiser la vitesse de convergence d'un algorithme pour réduire le coût de calcul (sobriété numérique) ?**
>   

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

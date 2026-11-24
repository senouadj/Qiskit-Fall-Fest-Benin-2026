# Projet 1 — Optimisation quantique de l'allocation des cultures au Bénin

**Qiskit Fall Fest 2026 • IndabaX Benin • Sèmè City**

**Auteur :** ADJOGAN Senou Gbenoukpo

---

## 1. Présentation du projet

Ce projet a été réalisé dans le cadre du **Qiskit Fall Fest 2026**, organisé au Bénin par IndabaX Benin et iSHEERO, avec le soutien d’IBM Quantum.

L’objectif est de montrer comment les techniques d’optimisation de l’informatique quantique (via Qiskit) peuvent être appliquées à un problème concret et utile pour le Bénin : **aider un agriculteur à choisir les meilleures cultures à planter** afin de maximiser son rendement, tout en respectant une contrainte de surface limitée.

---

## 2. Objectif

Décider quelles cultures planter parmi :
- Maïs
- Manioc
- Coton
- Arachide

de façon à **maximiser le rendement total** (exprimé en tonnes), sous la contrainte de ne pouvoir planter que **2 cultures maximum**.

---

## 3. Formulation du problème

### Variables de décision (binaires)
- `Mais` = 1 si on plante du maïs, sinon 0
- `Manioc` = 1 si on plante du manioc, sinon 0
- `Coton` = 1 si on plante du coton, sinon 0
- `Arachide` = 1 si on plante de l’arachide, sinon 0

### Fonction objectif (à maximiser)
Rendement = 3.5 × Mais + 12.0 × Manioc + 1.8 × Coton + 1.2 × Arachide

### Contrainte
Mais + Manioc + Coton + Arachide ≤ 2

---

## 4. Méthode utilisée

Le problème est modélisé avec la classe `QuadraticProgram` de **Qiskit Optimization**, puis résolu grâce à :

- `MinimumEigenOptimizer`
- `NumPyMinimumEigensolver`

Cette approche permet d’obtenir la solution optimale de manière fiable et de l’interpréter facilement.

---

## 5. Technologies utilisées

- Python 3
- Qiskit
- Qiskit Optimization
- Qiskit Algorithms
- NumPy

---

## 6. Résultats

Le programme affiche clairement :
- Les cultures recommandées (`OUI, planter` ou `NON`)
- Le rendement total estimé en tonnes

Cela permet à un agriculteur ou à un décideur de comprendre immédiatement la recommandation.

---

## 7. Comment exécuter le projet

### Installation des dépendances
```bash
pip install qiskit qiskit-aer qiskit-algorithms qiskit-optimization numpyLancementBashpython Projet1_Allocation_Cultures.py8.

Structure du code
Importation des bibliothèques
Création du problème d’optimisation (QuadraticProgram)
Déclaration des variables binaires (les cultures)
Définition de la fonction objectif (maximisation du rendement)
Ajout de la contrainte de surface
Résolution du problème
Affichage et interprétation des résultats en langage simple

9. Améliorations possibles
Intégrer le coût de l’engrais et de la main-d’œuvre
Prendre en compte la rotation des cultures
Utiliser de vraies données agricoles du Bénin
Étendre le modèle à plus de cultures et de contraintes
Tester l’algorithme sur un vrai processeur quantique IBM
Ajouter une interface simple pour l’utilisateur

10. Contexte de réalisationCe projet a été préparé en amont du Qiskit Fall Fest 2026 qui se tient le 28 novembre 2026 à Sèmè City (Bénin).Il s’inscrit dans une démarche de démonstration pratique : montrer que l’informatique quantique peut être mise au service de problématiques locales africaines.

11. AuteurADJOGAN Senou Gbenoukpo

Participant sélectionné au Qiskit Fall Fest 2026 – IndabaX Benin12. LicenceProjet réalisé dans un cadre éducatif et de démonstration.

Libre d’utilisation pour l’apprentissage et la présentation.

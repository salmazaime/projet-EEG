# Projet Exploitation du dataset CL-Drive

## Estimation de la charge cognitive du conducteur à partir des signaux EEG

### Contexte

Ce projet s'inscrit dans la continuité des travaux réalisés dans les TD1, TD2, TD3 et TD4 autour du dataset **CL-Drive**.

Les séances précédentes ont permis d'étudier :

* le protocole expérimental du dataset CL-Drive ;
* la compréhension de l'article scientifique associé ;
* la segmentation des signaux en fenêtres temporelles de 10 secondes ;
* le prétraitement des signaux EEG ;
* l'extraction des caractéristiques (features) EEG.

À l'issue du TD4, un ensemble de fichiers de caractéristiques EEG a été généré dans le dossier :

```text
EEG_Features_10s/
```

Ce projet ne traite plus l'extraction des features. Il exploite directement les caractéristiques déjà calculées afin de construire un pipeline complet d'apprentissage automatique pour l'estimation de la charge cognitive du conducteur.

---

## Objectif

L'objectif est de développer un pipeline supervisé permettant de prédire le niveau de charge cognitive à partir des signaux EEG.

Le pipeline suivi est le suivant :

```text
EEG_Features_10s
        │
        ▼
Normalisation des features
        │
        ▼
Normalized_Features_10s/EEG
        │
        ▼
Ajout des niveaux et labels
        │
        ▼
Normalized_Features_10s_With_Label/EEG
        │
        ▼
Construction du dataset supervisé
        │
        ▼
Entraînement des modèles de classification
        │
        ▼
Évaluation des performances
        │
        ▼
Interprétation des résultats
```

---

## Structure du projet

```text
.
├── TP.ipynb
├── TD4.ipynb
├── README.md
├── Data/
│   ├── EEG/
│   ├── Labels/
│   └── EEG_Features_10s/
│
├── Normalized_Features_10s/
│   └── EEG/
│
└── Normalized_Features_10s_With_Label/
    └── EEG/
```

---

## Méthodologie

Les principales étapes réalisées sont :

1. Chargement des fichiers de features EEG.
2. Normalisation des variables numériques.
3. Association des niveaux de charge cognitive.
4. Création des labels supervisés.
5. Construction du dataset d'apprentissage.
6. Séparation des données d'entraînement et de test.
7. Entraînement de modèles de classification.
8. Évaluation des performances à l'aide de métriques adaptées.
9. Analyse et interprétation des résultats obtenus.

---

## Technologies utilisées

* Python 3
* Jupyter Notebook
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

## Données

Le dataset CL-Drive n'est pas inclus dans ce dépôt GitHub en raison de sa taille importante.

Pour exécuter le projet, les données doivent être placées dans la structure de dossiers attendue décrite dans le sujet du TP.

---

## Résultat attendu

À la fin du projet, le système doit être capable d'estimer automatiquement le niveau de charge cognitive du conducteur à partir des caractéristiques EEG extraites du dataset CL-Drive.

---

## Auteurs 

Salma Zaime et Omar El Mojahid

Projet réalisé dans le cadre du module d'Interfaces Cerveau-Machine.

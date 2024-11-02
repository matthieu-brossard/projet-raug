# Visualiseur de protéines (Projet Réalité augmentée)

## Membre du groupe

Brossard Matthieu et Chen Cyril

## Introduction du projet

Ce projet est une application web de visualisation de protéines utilisant Three.js. Il permet de charger et d'afficher des modèles 
de protéines en 3D à partir des fichiers fournis par AlphaFold. Ce visualiseur représente les atomes et les
liaisons des protéines de manière interactive avec la possibilité justement de manipuler la vue en 3D pour explorer la structure du molécule.

## Fonctionnalités

- Un chargement dynamique de protéines en entrant un identifiant de protéine pour charger un modèle 3D en direct depuis AlphaFold.
- On peut visualiser les atomes et les liaisons directement en 3D avec des couleurs distinctes pour chaque 
type d'élément chimique (carbone, oxygène, azote, etc.).
- On peut contrôler la vue pour explorer la structure de la protéine sous différents angles.

## Technologies utilisées

Nous avons utilisé Three.js pour effectuer ce projet. Cette outils nous a permis de modéliser des objets en 3D directement sur le Web.

## Compilation du projet et utilisation

- Lancez index.html dans un navigateur web compatible (Google chrome).
- Vous allez avoir par défaut un molécule mais vous pouvez mettre d'autre molécule dans le champ saisie l'identifiant d'une protéine au
format AF-Pxxxxxx-F1-model_v1 (par exemple : AF-P69905-F1-model_v1 pour l'hémoglobine).
- Une fois chargée, la protéine sera affichée en 3D et vous pourrez utiliser la souris pour faire pivoter, zoomer et explorer la structure du molécule.

## Détails du Code

- Le code JavaScript initialise une scène Three.js avec une caméra, un contrôleur d'orbite et un système de rendu. 
Il crée ensuite des objets 3D pour chaque atome de la protéine et les positionne selon les données de coordonnées du fichier .pdb.
- La fonction parsePDB analyse les données PDB pour extraire les coordonnées et les types d’atomes.
- Chaque atome est représenté par une sphère colorée selon son type chimique :
> Carbone (C) : Vert |
> Oxygène (O) : Rouge |
> Azote (N) : Bleu |
> Autres : Blanc

- Les liaisons covalentes sont représentées par des cylindres entre les atomes, en fonction des distances interatomiques et des seuils de liaison spécifiques pour chaque élément.

## Ressource

Les modèles de protéines sont téléchargés à partir d'AlphaFold, une base de données de structures de protéines.

## Rendu

- Projet pour le cours Réalité Augmentée MAJEURE SANTÉ
- Date du rendu Dimanche 3 Novembre à 13H


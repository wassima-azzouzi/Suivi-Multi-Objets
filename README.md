# Détection et Suivi Multi-Objets (MOT) en Temps Réel (DeepSORT et YOLO)

Ce projet implémente un système puissant de détection et de suivi d'objets en combinant **YOLOv8** (pour une détection ultra-rapide) et **DeepSORT** (pour un suivi robuste avec identifiants uniques).

![Detection Example](https://img.shields.io/badge/YOLO-v8-blue) ![Tracking](https://img.shields.io/badge/Tracking-DeepSORT-green)

##  Fonctionnalités Détaillées

###  Détection avec YOLOv8
Le modèle **YOLOv8** (You Only Look Once) assure la détection d'objets en une seule passe, offrant une rapidité exceptionnelle.
- **Multi-Classes** : Capacité de détecter simultanément des **personnes**, **voitures**, **bus**, **motos**, etc.
- **Précision** : Localisation exacte des objets via des boîtes de délimitation (bounding boxes).

###  Suivi (Tracking) avec DeepSORT
L'algorithme **DeepSORT** ajoute une dimension temporelle à la détection :
- **Identification Unique** : Attribue un identifiant persistant à chaque objet (ex: **Car ID 1**, **Car ID 3**, **Person ID 12**).
- **Séparation de Même Classe** : Permet de distinguer deux objets identiques (ex: deux voitures rouges) grâce à leurs vecteurs de mouvement et d'apparence.
- **Robustesse** : Gère les occlusions temporaires (si un objet passe derrière un autre, il garde le même ID à sa réapparition).

###  Comptage de Véhicules
Le système inclut une logique de **comptage automatique** :
- Suivi du nombre total de véhicules ayant traversé une zone spécifique.
- Distinction par classe pour des statistiques précises sur le flux de trafic.



## 🛠 Installation

1. Clonez ce dépôt.
2. Installez les dépendances :
   ```bash
   pip install ultralytics torch torchvision opencv-python
   ```
3. Téléchargez les fichiers DeepSORT requis (instructions fournies dans le notebook).

##  Structure du Projet

- `version_final_YOLOv8_TP9 .ipynb` : Le notebook principal contenant toute la logique.
- `README.md` : Documentation du projet.
- `.gitignore` : Gestion des fichiers à exclure du versionnage.

##  Utilisation

Ouvrez le fichier Jupyter Notebook et exécutez les cellules séquentiellement. Le notebook s'occupera de :
- Cloner le dépôt de base.
- Configurer les dossiers.
- Appliquer les patchs de correction.
- Lancer l'inférence sur votre vidéo.

---
*Réalisé dans le cadre d'un projet de détection d'objets avancée.*

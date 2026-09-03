Analyse Automatisée de Formulaires Clients
Ce projet automatise l'extraction des choix cochés sur des formulaires clients papier scannés ou photographiés, puis génère des statistiques et des visualisations graphiques des préférences clients.

Fonctionnalités
Détection automatique par IA : Utilise un modèle de vision par ordinateur (YOLO) pour localiser et classifier les cases (checked / unchecked) sur chaque image.

Traitement par lots : Parcourt un dossier entier de formulaires (un par client) pour industrialiser l'analyse.

Structuration par sections : Analyse trois sections clés du formulaire :

type_quittance (Comptant, Règlement, Terme)

sous_branche (Individuel à la carte, Trik Slema, Véhicule étranger, Flottes)

type_pack (Inconnu, SÉCURITÉ, SÉCURITÉ +, SÉRÉNITÉ, SUPER SÉCURITÉ)

Rapports et exports :

Fichier de données brutes consolidé (resultats_clients.csv)

Résumé textuel des pourcentages par catégorie

Graphique à barres des tendances (preferences_clients.png)

Prérequis et Installation
Le script s'exécute idéalement dans Google Colab ou un environnement Python disposant des bibliothèques suivantes :

Bash
pip install -q ultralytics huggingface_hub pillow pandas matplotlib
Guide d'Utilisation
Préparer les données : Créez un dossier nommé scans_clients/ dans votre environnement de travail.

Ajouter les images : Déposez-y les photos ou scans des formulaires remplis (formats acceptés : .png, .jpg, .jpeg). Nommez-les librement (ex: client_001.jpg, client_002.jpg).

Exécuter le script : Copiez-collez l'intégralité du code dans une cellule Python et lancez-le.

Fichiers Produits
resultats_clients.csv : Tableau récapitulatif contenant une ligne par client avec l'ensemble de ses choix validés.

preferences_clients.png : Visualisation graphique des options les plus plébiscitées pour chaque section.

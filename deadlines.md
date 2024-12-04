# Calendrier des Deadlines (14 semaines, 10h/semaine)

## Semaine 1
- Préparer le serveur sans GPU pour l'installation de Proxmox :
  - Télécharger Proxmox, créer la clé USB bootable, configurer le BIOS.
- Configurer le routeur pour des IP fixes (serveur sans GPU, NAS).
- Installer Proxmox sur le serveur sans GPU :
  - Configurer le réseau basique (IP statique), test de connectivité avec le NAS.

## Semaine 2
- Créer une VM Debian pour le routeur (via Proxmox et Ansible).
- Déployer et configurer les services réseau sur le routeur :
  - Nginx Proxy Manager, Pi-Hole, Fail2Ban.
- Tester et valider les configurations réseau.
- Installer Ansible et configurer l’inventaire (routeur, serveur sans GPU, NAS).

## Semaine 3
- Créer une VM pour l’automatisation et le monitoring sur le serveur sans GPU.
- Déployer les services de base sur le serveur sans GPU :
  - Docker, Portainer, Redis.
- Héberger le blog technique (Hugo) :
  - Configurer une VM ou un conteneur dédié.
  - Ajouter le blog au reverse proxy pour un accès sécurisé.

## Semaine 4
- Développer un backend de gestion de tâches avec Ansible en **Go** :
  - Endpoints pour créer/arrêter les services avec Ansible.
  - Gestion des timers pour les arrêts automatiques.
- Finaliser l’intégration des services réseau avec le monitoring :
  - Prometheus, Grafana, Node Exporter.
- Ajouter une interface web légère pour l’application en Go (Vue.js).

## Semaine 5
- Configurer Docker Registry et Drive sur le NAS.
- Déployer l’application de recommandation existante (backend Python, API et scraping).
- Commencer à développer une web-app frontend en **Vue.js** pour l’application de recommandation.

## Semaine 6
- Développer le module d’entraînement IA en **Julia** :
  - Préprocessing des données et entraînement basique via Flux.jl ou MLJ.jl.
- Créer une API backend en Python (FastAPI) pour orchestrer les tâches d’entraînement IA :
  - Endpoint pour uploader les datasets et sélectionner la cible.
  - Endpoint pour récupérer les modèles.

## Semaine 7
- Ajouter une interface pour visualiser les métriques de l’entraînement IA (Vue.js).
- Tester et optimiser les performances des modèles sur le serveur GPU.
- Finaliser le frontend pour l’application de recommandation.

## Semaine 8
- Développer une API backend pour le générateur de médias personnalisé en **Rust** :
  - Générer des textes avec GPT-like.
  - Générer des schémas ou images avec Stable Diffusion.
- Créer un pipeline pour intégrer les médias générés dans le blog technique.
- Intégrer l’application de recommandation au reverse proxy et au monitoring.

## Semaine 9
- Ajouter une interface utilisateur (Vue.js) pour soumettre des requêtes au générateur de médias.
- Développer une application backend pour la visualisation de graphes en **Haskell** :
  - Fournir des APIs pour interagir avec les graphes.
- Tester le backend de graphe avec des datasets simples (microservices ou données vectorielles).

## Semaine 10
- Créer un frontend pour les graphes dynamiques avec D3.js ou Cytoscape.js.
- Tester l’ensemble des fonctionnalités de visualisation de graphes :
  - Relations entre microservices.
  - Exploration des relations entre données vectorielles.
- Déployer l’application de graphes sur le homelab.

## Semaine 11
- Commencer à développer l’analyseur de logs en **Scala** :
  - Agrégation des logs depuis plusieurs services via Fluentd ou Logstash.
  - Analyse et extraction des patterns dans les logs.
- Exporter les résultats des logs vers Grafana pour la visualisation.

## Semaine 12
- Finaliser l’analyseur de logs distribué en Scala :
  - Ajouter des alertes en cas d’anomalies détectées.
- Intégrer l’analyseur au monitoring global via Prometheus et Grafana.
- Tester l’interconnexion de tous les services hébergés.

## Semaine 13
- Réaliser des tests finaux sur tous les services déployés :
  - Blog technique, gestion de tâches, recommandation, entraînement IA, générateur de médias, visualisation de graphes.
- Intégrer les services dans une page d’accueil centralisée avec le reverse proxy.
- Monitorer les performances des services via Grafana.

## Semaine 14
- Finaliser la documentation de tous les services :
  - Tutoriels d’installation et d’utilisation.
  - Schémas techniques pour chaque projet.
- Présenter les résultats dans un portfolio en ligne :
  - Démonstration des services hébergés.
  - Évaluation des technologies et langages utilisés.

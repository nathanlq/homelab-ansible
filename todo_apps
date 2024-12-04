# Todo List - Services Complémentaires

## 1. Hébergement du Blog Technique (Prioritaire, rapide à mettre en place)
- [ ] Configurer une VM ou un conteneur pour héberger le blog.
- [ ] Déployer le blog généré statiquement (Hugo) sur la VM ou via Docker.
- [ ] Ajouter une tâche Ansible pour :
  - [ ] Automatiser les mises à jour des articles.
  - [ ] Planifier des sauvegardes régulières.
- [ ] Ajouter l’entrée dans le reverse proxy (Nginx Proxy Manager) pour un accès sécurisé.

---

## 2. Application de Gestion de Tâches avec Ansible
- **Objectif Langage : Go**
  - [ ] Développer un backend en **Go** pour interagir avec Ansible :
    - [ ] Endpoint pour créer des services avec des playbooks spécifiques.
    - [ ] Endpoint pour arrêter les services.
    - [ ] Gestion des timers pour des arrêts automatiques.
  - [ ] Ajouter une interface web légère (React ou Vue.js) pour gérer les services :
    - [ ] Liste des services en cours.
    - [ ] Boutons pour démarrer/arrêter les services.
  - [ ] Tester et intégrer le tout avec vos playbooks Ansible existants.
  - [ ] Documenter les API et créer des exemples d’utilisation (ex : déploiement de VSCode Server).

---

## 3. Serveur d’Entraînement Automatique pour IA
- **Objectif Langage : Julia**
  - [ ] Développer un module d’entraînement en **Julia** pour gérer les tâches d’entraînement :
    - [ ] Transformation des datasets et preprocessing.
    - [ ] Entraînement des modèles via Flux.jl ou MLJ.jl.
    - [ ] Export des modèles pour une utilisation dans Python ou autre environnement.
  - [ ] Créer une API backend (FastAPI en Python) pour orchestrer les tâches :
    - [ ] Endpoint pour uploader les datasets.
    - [ ] Sélection de la cible (colonne à prédire).
    - [ ] Endpoint pour récupérer le modèle final.
  - [ ] Ajouter une interface simple (Vue.js) pour visualiser les métriques (accuracy, confusion matrix).
  - [ ] Tester et optimiser les performances sur le serveur GPU.

---

## 4. Générateur de Médias Personnalisé avec IA
- **Objectif Langage : Rust**
  - [ ] Développer une API backend en **Rust** (framework comme Actix Web) pour :
    - [ ] Générer des textes avec GPT-like.
    - [ ] Générer des schémas ou images avec Stable Diffusion.
  - [ ] Créer un pipeline automatisé pour intégrer les résultats générés dans le blog.
  - [ ] Ajouter une interface pour soumettre des requêtes textuelles (Vue.js pour le frontend).
  - [ ] Documenter les modèles utilisés et les résultats obtenus.

---

## 5. Hébergement de l’Application de Recommandation et Recherche
- [ ] Déployer l’application existante (scraping, organisation vectorielle avec pgvector et API de recherche).
- **Objectif Langage : Vue.js (Frontend)**
  - [ ] Développer une web-app frontend en **Vue.js** pour les recommandations :
    - [ ] Barre de recherche avancée.
    - [ ] Suggestions basées sur la similarité vectorielle.
    - [ ] Historique des recherches ou favoris.
- [ ] Ajouter un tableau de bord pour monitorer les performances des recommandations.

---

## 6. Outil de Visualisation de Graphe Dynamique
- **Objectif Langage : Haskell**
  - [ ] Développer une application backend en **Haskell** pour :
    - [ ] Construire les structures de graphes (librairie comme FGL).
    - [ ] Fournir des APIs pour interagir avec les graphes (ajout/suppression de nœuds, relations).
  - **Frontend : Vue.js ou D3.js**
    - [ ] Utiliser une bibliothèque pour afficher les graphes dynamiques.
  - [ ] Tester avec des cas simples :
    - [ ] Relations entre les microservices de votre homelab.
    - [ ] Exploration des relations entre vos données vectorielles (recherches similaires).

---

## Nouveaux Projets pour Explorer Scala
### 7. Analyseur de Logs Distribué
- **Objectif Langage : Scala**
  - [ ] Développer une application en **Scala** pour analyser les logs de vos services :
    - [ ] Agrégation des logs depuis plusieurs services (via Fluentd ou Logstash).
    - [ ] Analyse et extraction des patterns dans les logs (Spark ou Akka Streams).
  - [ ] Exporter les résultats dans Grafana pour la visualisation.
  - [ ] Ajouter des alertes en cas d’anomalies détectées.

---

## Éléments Transversaux
- [ ] Intégrer chaque service dans votre infrastructure existante :
  - [ ] Gestion centralisée des accès via le reverse proxy (Nginx Proxy Manager).
  - [ ] Monitoring des ressources via Prometheus/Grafana.
  - [ ] Planification des sauvegardes régulières (base de données, configurations, modèles IA).
- [ ] Documenter chaque service avec des schémas techniques et des tutoriels d’utilisation.

## Résumé des Langages et Technologies :
1. **Go** : Backend pour la gestion des tâches avec Ansible.
2. **Julia** : Modules d’entraînement IA pour le serveur automatique.
3. **Rust** : Générateur de médias personnalisé.
4. **Vue.js** : Frontend pour le blog et les recommandations.
5. **Haskell** : Backend pour l’outil de visualisation de graphes.
6. **Scala** : Analyseur de logs distribué.

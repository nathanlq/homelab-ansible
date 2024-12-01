# Todo List - Homelab

## 1. Préparation de l'infrastructure
- [ ] Préparer les deux serveurs pour l'installation de Proxmox.
  - [ ] Télécharger la dernière version de Proxmox VE.
  - [ ] Créer une clé USB bootable.
  - [ ] Configurer le BIOS pour activer la virtualisation.
- [ ] Installer Proxmox sur les deux serveurs.
  - [ ] Configurer le réseau basique (IP statique).
  - [ ] Vérifier la connectivité entre les serveurs et le NAS Synology.
- [ ] Configurer le routeur pour des IP fixes sur les serveurs et le NAS.

## 2. Configuration d’Ansible
- [ ] Installer Ansible sur le poste de gestion.
- [ ] Configurer l’inventaire pour les serveurs et VMs.
  - [ ] Définir les groupes (routeur, serveur avec GPU, serveur sans GPU, NAS).
- [ ] Créer des playbooks pour automatiser la configuration des services.

## 3. Création des VMs
- [ ] Sur le routeur :
  - [ ] Créer une VM Debian avec les ressources nécessaires via Proxmox et Ansible.
  - [ ] Ajouter cette VM à l’inventaire Ansible.
- [ ] Sur le serveur avec GPU :
  - [ ] Créer une VM pour les services de développement et d’hébergement LLM.
  - [ ] Ajouter cette VM à l’inventaire Ansible.
- [ ] Sur le serveur sans GPU :
  - [ ] Créer une VM pour l’automatisation, le monitoring, et les bases de données.
  - [ ] Ajouter cette VM à l’inventaire Ansible.

## 4. Configuration des services via Ansible
### VM Routeur
- [ ] Créer un playbook Ansible pour installer et configurer :
  - [ ] Nginx Proxy Manager (reverse proxy pour HTTPS).
  - [ ] Squid (proxy pour accélération).
  - [ ] Pi-Hole (blocage publicitaire et DNS).
  - [ ] Fail2Ban (sécurité).
- [ ] Tester et valider les configurations réseau.

### Serveur avec GPU
- [ ] Créer un playbook Ansible pour installer et configurer :
  - [ ] Docker et Portainer pour la gestion des conteneurs.
  - [ ] VSCode Server (IDE web).
  - [ ] JupyterHub (web notebooks).
  - [ ] Hébergement LLM :
    - [ ] Starcoder / Code Llama (code).
    - [ ] Mistral (généraliste).
  - [ ] API pour les LLM.
- [ ] Ajouter les services au reverse proxy.

### Serveur sans GPU
- [ ] Créer un playbook Ansible pour installer et configurer :
  - [ ] Docker et Portainer pour la gestion des conteneurs.
  - [ ] LSO (orchestrateur).
  - [ ] Sourcehut (code hosting et CI/CD).
  - [ ] Monitoring :
    - [ ] Prometheus.
    - [ ] Grafana.
    - [ ] Node Exporter.
  - [ ] Redis (fast DB).
- [ ] Ajouter les services au reverse proxy.

## 5. Gestion du stockage
### NAS Synology
- [ ] Configurer et activer les services intégrés :
  - [ ] Docker Registry.
  - [ ] Drive.
- [ ] Créer et configurer les applications du NAS :
  - [ ] PostgreSQL (avec pgvector).
  - [ ] FTP et Rsync.
- [ ] Héberger un site web statique pour le portfolio.

### Serveur sans GPU
- [ ] Configurer Redis (fast DB).

## 6. Création d’une page d’accueil
- [ ] Créer une page d’accueil pour le homelab via un conteneur web.
  - [ ] Lister tous les services avec des liens directs.
  - [ ] Ajouter des icônes et descriptions pour chaque service.
  - [ ] Héberger la page d’accueil sur le reverse proxy avec un accès HTTPS.
  - [ ] Intégrer une vue d’ensemble des ressources (via Prometheus/Grafana).

## 7. Tests et finalisation
- [ ] Vérifier que tous les services sont accessibles et fonctionnent.
- [ ] Monitorer les performances et ajuster les ressources des VMs si nécessaire.
- [ ] Sauvegarder les configurations et playbooks Ansible.
- [ ] Documenter les configurations pour maintenance future.

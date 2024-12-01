# Todo List - Homelab

## 1. Préparation de l'infrastructure (Prioritaire)
- [ ] Préparer le serveur sans GPU pour l'installation de Proxmox.
  - [ ] Télécharger la dernière version de Proxmox VE.
  - [ ] Créer une clé USB bootable.
  - [ ] Configurer le BIOS pour activer la virtualisation.
- [ ] Installer Proxmox sur le serveur sans GPU.
  - [ ] Configurer le réseau basique (IP statique).
  - [ ] Vérifier la connectivité entre le serveur sans GPU et le NAS Synology.
- [ ] Configurer le routeur pour des IP fixes sur le serveur sans GPU et le NAS.

## 2. Configuration d’Ansible (Débuter maintenant)
- [ ] Installer Ansible sur le poste de gestion.
- [ ] Configurer l’inventaire pour les serveurs et VMs déjà disponibles.
  - [ ] Définir les groupes (routeur, serveur sans GPU, NAS).
- [ ] Créer des playbooks initiaux pour les services réalisables :
  - [ ] Services réseau sur le routeur (Nginx Proxy Manager, Pi-Hole, etc.).
  - [ ] Automatisation et monitoring sur le serveur sans GPU.

## 3. Création des VMs (Sans serveur GPU)
- [ ] Sur le routeur :
  - [ ] Créer une VM Debian avec les ressources nécessaires via Proxmox et Ansible.
  - [ ] Ajouter cette VM à l’inventaire Ansible.
- [ ] Sur le serveur sans GPU :
  - [ ] Créer une VM pour l’automatisation et le monitoring.
  - [ ] Ajouter cette VM à l’inventaire Ansible.

## 4. Configuration des services via Ansible (Sans serveur GPU)
### VM Routeur
- [ ] Créer un playbook Ansible pour installer et configurer :
  - [ ] Nginx Proxy Manager (reverse proxy pour HTTPS).
  - [ ] Squid (proxy pour accélération).
  - [ ] Pi-Hole (blocage publicitaire et DNS).
  - [ ] Fail2Ban (sécurité).
- [ ] Tester et valider les configurations réseau.

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

## 5. Gestion du stockage (NAS Synology)
- [ ] Configurer et activer les services intégrés du NAS :
  - [ ] Docker Registry.
  - [ ] Drive.
- [ ] Créer et configurer les applications du NAS :
  - [ ] PostgreSQL (avec pgvector).
  - [ ] FTP et Rsync.
- [ ] Héberger un site web statique pour le portfolio.

## 6. Préparation pour le serveur avec GPU (En attente de réception)
- [ ] Configurer Proxmox une fois le serveur reçu.
- [ ] Créer une VM pour les services de développement et d’hébergement LLM.
- [ ] Ajouter cette VM à l’inventaire Ansible.
- [ ] Créer un playbook Ansible pour :
  - [ ] VSCode Server (IDE web).
  - [ ] JupyterHub (notebooks collaboratifs).
  - [ ] Hébergement de LLM (Starcoder / Code Llama, Mistral).
  - [ ] API pour les LLM.
- [ ] Ajouter les services GPU au reverse proxy.

## 7. Création d’une page d’accueil (Réalisable maintenant)
- [ ] Créer une page d’accueil pour le homelab via un conteneur web.
  - [ ] Lister tous les services avec des liens directs.
  - [ ] Ajouter des icônes et descriptions pour chaque service.
  - [ ] Ajouter une vue d’ensemble des ressources (via Prometheus/Grafana).
  - [ ] Héberger la page d’accueil sur le reverse proxy avec un accès HTTPS.

## 8. Tests et finalisation (Au fur et à mesure)
- [ ] Vérifier que tous les services sont accessibles et fonctionnent.
- [ ] Monitorer les performances et ajuster les ressources des VMs si nécessaire.
- [ ] Sauvegarder les configurations et playbooks Ansible.
- [ ] Documenter les configurations pour maintenance future.

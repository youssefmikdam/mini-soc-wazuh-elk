# Déploiement du Serveur Wazuh (Docker)

## Architecture
Pour optimiser les ressources, le serveur SOC a été déployé sur une machine Kali Linux via **Docker** et **Docker Compose**. Cela permet une mise en place rapide et isolée des composants :
- **Wazuh Manager** (Analyse)
- **Wazuh Indexer** (Base de données / Elasticsearch)
- **Wazuh Dashboard** (Interface Web / Kibana)

## Pré-requis Système
Avant le lancement, la mémoire virtuelle de l'hôte a été configurée pour supporter la stack ELK :
```bash
sysctl -w vm.max_map_count=262144

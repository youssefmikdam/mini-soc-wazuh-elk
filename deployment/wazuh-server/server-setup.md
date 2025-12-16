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
Installation
Le déploiement s'est fait via le dépôt officiel. Voici les commandes utilisées :

Clonage du dépôt :

Bash

git clone [https://github.com/wazuh/wazuh-docker.git](https://github.com/wazuh/wazuh-docker.git) -b v4.9.0
Génération des certificats SSL :

Bash

docker-compose -f generate-indexer-certs.yml run --rm generator
Démarrage des services :

Bash

docker-compose up -d
